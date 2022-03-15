---
layout: post
title: Agenda view in .NET MAUI Scheduler control | Syncfusion
description: Learn here all about the Agenda view feature of Syncfusion .NET MAUI Scheduler (SfScheduler) control and more.
platform: maui
control: SfScheduler
documentation: ug
---

# Agenda view in .NET MAUI Scheduler (SfScheduler)

The agenda view displays a list of scheduled appointments grouped by week, between set minimum and maximum dates, with the appointments from the current date displayed by default. When the `AppointmentsSource` property of `SfScheduler` is null, the agenda view will show only the month, week, and date headers.

A agenda view displays different UI for mobile and desktop, for mobile it displays the month header, the week header, and the date header however for desktop, it displays the appointment only.

N> When the desktop view width is less than 600, the scheduler will display the mobile agenda UI on the desktop.

## Appointment text customization

The appointment text style can be customized by using the `AppointmentTextStyle` property of the `SfScheduler.`

{% tabs %}
{% highlight xaml %}

 <scheduler:SfScheduler x:Name="Scheduler" 
                        View="Agenda">
 </scheduler:SfScheduler>

{% endhighlight %}
{% highlight c# %}

this.Scheduler.View = SchedulerView.Agenda;
// Creating an instance for the scheduler appointment collection.
var appointments = new ObservableCollection<SchedulerAppointment>();
// Adding scheduler appointment in the scheduler appointment collection.
appointments.Add(new SchedulerAppointment()
{
    Subject = "Meeting",
    StartTime = DateTime.Now,
    EndTime = DateTime.Now.AddHours(1),
    RecurrenceRule = "FREQ=DAILY;INTERVAL=1",
    Background = Brush.Orange,
});
// Adding scheduler appointment in the scheduler appointment collection.
this.Scheduler.AppointmentsSource = appointments;
// Creating the text style for the appointments.
var appointmentTextStyle = new SchedulerTextStyle()
{
    TextColor = Colors.White,
    FontSize = 12,
};
// Setting the text style for the appointments.
this.Scheduler.AppointmentTextStyle = appointmentTextStyle;

{% endhighlight %}
{% endtabs %}

## Day header customization

The day header can be customized by using the `DayHeaderSettings` property of `AgendaView` in the `SfScheduler.`

You can style the day format, day text style, date text style, and background color by using the properties such as `DayFormat,` `DayTextStyle,` `DateTextStyle,` and `Background` properties of `DayHeaderSettings.`

{% tabs %}
{% highlight xaml %}

 <scheduler:SfScheduler x:Name="Scheduler"
                        View="Agenda">
    <scheduler:SfScheduler.AgendaView>
        <scheduler:SchedulerAgendaView>
            <scheduler:SchedulerAgendaView.DayHeaderSettings>
                <scheduler:SchedulerDayHeaderSettings DayFormat="MM, ddd"
                                                      Background="LightGreen"/>
            </scheduler:SchedulerAgendaView.DayHeaderSettings>
        </scheduler:SchedulerAgendaView>
    </scheduler:SfScheduler.AgendaView>
 </scheduler:SfScheduler>

{% endhighlight %}
{% highlight c# %}

this.Scheduler.View = SchedulerView.Agenda;
var textStyle = new SchedulerTextStyle()
{
    TextColor = Colors.Red,
    FontSize = 12,
};

this.Scheduler.AgendaView.DayHeaderSettings.DayFormat = "MM, ddd";
this.Scheduler.AgendaView.DayHeaderSettings.DayTextStyle = textStyle;
this.Scheduler.AgendaView.DayHeaderSettings.DateTextStyle = textStyle;
this.Scheduler.AgendaView.DayHeaderSettings.Background = Brush.LightGreen;

{% endhighlight %}
{% endtabs %}

N> The default value of `DayFormat` is `MMM, ddd.`

## Week header customization

The week header can be customized by using the `WeekHeaderSettings` property of `AgendaView` in the `SfScheduler.`

You can style the date format, height, text style, and background color by using the properties such as `DateFormat,` `Height,` `TextStyle,` and `Background` properties of `WeekHeaderSettings.`

{% tabs %}
{% highlight xaml %}

 <scheduler:SfScheduler x:Name="Scheduler"
                        View="Agenda">
    <scheduler:SfScheduler.AgendaView>
        <scheduler:SchedulerAgendaView>
            <scheduler:SchedulerAgendaView.WeekHeaderSettings>
                <scheduler:SchedulerWeekHeaderSettings  DateFormat="MM, ddd"
                                                        Height="100"
                                                        Background="LightGreen" />
            </scheduler:SchedulerAgendaView.WeekHeaderSettings>
        </scheduler:SchedulerAgendaView>
    </scheduler:SfScheduler.AgendaView>
 </scheduler:SfScheduler>

{% endhighlight %}
{% highlight c# %}

this.Scheduler.View = SchedulerView.Agenda;
var textStyle = new SchedulerTextStyle()
{
    TextColor = Colors.Red,
    FontSize = 12,
};

this.Scheduler.AgendaView.WeekHeaderSettings.DateFormat = "MM, ddd";
this.Scheduler.AgendaView.WeekHeaderSettings.Height = 100;
this.Scheduler.AgendaView.WeekHeaderSettings.TextStyle = textStyle;
this.Scheduler.AgendaView.WeekHeaderSettings.Background = Brush.LightGreen;

{% endhighlight %}
{% endtabs %}

N> 
* The default value of `DateFormat,` and `Height` are `MMM dd,` and `30` respectively.
* For desktop UI, The agenda view displays the appointment only.

## Month header customization

The month header can be customized by using the `MonthHeaderSettings` property of `AgendaView` in the `SfScheduler.`

### Customize Month header appearance using Style

You can style the date format, height, text style, and background color by using the properties such as `DateFormat,` `Height,` `TextStyle,` and `Background` properties of `MonthHeaderSettings.`

{% tabs %}
{% highlight xaml %}

 <scheduler:SfScheduler x:Name="Scheduler"
                        View="Agenda">
    <scheduler:SfScheduler.AgendaView>
        <scheduler:SchedulerAgendaView>
            <scheduler:SchedulerAgendaView.MonthHeaderSettings>
                <scheduler:SchedulerMonthHeaderSettings DateFormat="MMM yyy"
                                                        Height="200"
                                                        Background="LightGreen" />
            </scheduler:SchedulerAgendaView.MonthHeaderSettings>
        </scheduler:SchedulerAgendaView>
    </scheduler:SfScheduler.AgendaView>
 </scheduler:SfScheduler>

{% endhighlight %}
{% highlight c# %}

this.Scheduler.View = SchedulerView.Agenda;
var textStyle = new SchedulerTextStyle()
{
    TextColor = Colors.Red,
    FontSize = 12,
};

this.Scheduler.AgendaView.MonthHeaderSettings.DateFormat = "MMM yyy";
this.Scheduler.AgendaView.MonthHeaderSettings.Height = 200;
this.Scheduler.AgendaView.MonthHeaderSettings.TextStyle = textStyle;
this.Scheduler.AgendaView.MonthHeaderSettings.Background = Brush.LightGreen;

{% endhighlight %}
{% endtabs %}

### Customize Month header appearance using DataTemplate

You can customize the header appearance of scheduler by using the `MonthHeaderTemplate` property of `AgendaView.`

{% tabs %}
{% highlight xaml %}

  <scheduler:SfScheduler x:Name="Scheduler"
                         View="Agenda">
    <scheduler:SfScheduler.AgendaView>
        <scheduler:SchedulerAgendaView>
            <scheduler:SchedulerAgendaView.MonthHeaderTemplate>
                <DataTemplate>
                    <Grid>
                        <Label x:Name="label" HorizontalOptions="Center" Background="LightGreen" VerticalOptions="Center" TextColor="Black" FontSize="16"  Text="{Binding StringFormat='{0:MMMM yyyy}'}" />
                    </Grid>
                </DataTemplate>
            </scheduler:SchedulerAgendaView.MonthHeaderTemplate>
        </scheduler:SchedulerAgendaView>
    </scheduler:SfScheduler.AgendaView>
 </scheduler:SfScheduler>

{% endhighlight %}
{% endtabs %}

N> 
* The default value of `DateFormat,` and `Height` are `MMMM yyyy,` and `150` respectively.
* For desktop UI, The agenda view displays the appointment only.