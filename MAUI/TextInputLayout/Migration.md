---
layout: post
title: Migrating from Xamarin to .NET MAUI SfTextInputLayout | Syncfusion 
description: Learn all about Migrating from Syncfusion Xamarin TextInputLayout to Syncfusion .NET MAUI TextInputLayout control and more here.
platform: maui
control: SfTextInputLayout
documentation: ug
---  

# Migrating from Xamarin TextInputLayout to .NET MAUI TextInputLayout.

To migrate easier from Xamarin SfTextInputLayout to [.NET MAUI SfTextInputLayout](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Inputs.SfTextInputLayout.html), we kept most of the APIs from Xamarin SfTextInputLayout in MAUI SfTextInputLayout. However, to maintain the consistency of API naming in MAUI SfTextInputLayout, we renamed some of the APIs. The APIs changed in MAUI SfTextInputLayout from Xamarin SfTextInputLayout as detailed in the following:

## Namespaces 

<table>
<tr>
<th>Xamarin SfTextInputLayout</th>
<th>.NET MAUI SfTextInputLayout</th></tr>
<tr>
<td>Syncfusion.SfTextInputLayout.XForms</td>
<td>Syncfusion.Maui.Core</td></tr>
</table>

## Properties

<table> 
<tr>
<th>Xamarin SfTextInputLayout</th>
<th>.NET MAUI SfTextInputLayout</th>
<th>Description</th></tr>
<tr>
<td> {{'[FocusedBorderWidth]'| markdownify }} </td>
<td> {{'[FocusedStrokeThickness]'| markdownify }}</td>
<td>Gets or sets a value to customize the stroke thickness in a focused state. It is applicable for the bottom line and outline border when setting the container type as filled and outlined, respectively.</td></tr>
<tr>
<td> {{'[UnfocusedBorderWidth]'| markdownify }}</td>
<td> {{'[UnfocusedStrokeThickness]'| markdownify }}</td>
<td>Gets or sets a value to customize the stroke thickness in an unfocused state. It is applicable for the bottom line and outline border when setting the container type as filled and outlined, respectively.</td></tr>
<tr>
<td>{{'[FocusedColor]'| markdownify }}<br/> {{'[UnfocusedColor]'| markdownify }}<br/>{{'[ErrorColor]'| markdownify }}</td>
<td>{{'[Stroke]'| markdownify }}</td>
<td>Gets or sets the border color or base line color based on container and its states.</td></tr>
</table> 

## Classes

<table>
<tr>
<th>Class</th>
<th>Xamarin LabelStyle</th>
<th>.NET MAUI LabelStyle</th>
<th>Description</th></tr>
<tr>
<td>{{'[LabelStyle]'| markdownify }} </td>
<td>{{'[Color]'| markdownify }} </td>
<td> {{'[TextColor]'| markdownify }}</td>
<td>Gets or sets the text color of the SfTextInputLayout controls label.</td></tr>
</table>