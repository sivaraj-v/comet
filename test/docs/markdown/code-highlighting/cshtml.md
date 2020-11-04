# This is a test of the cshtml highlighter

## From Magic Folder Status

```cshtml
<%@ Page Title="Single Job" Language="C#" MasterPageFile="~/Site.master" AutoEventWireup="true"
    CodeBehind="AbortJob.aspx.cs" Inherits="MagicFolderStatus._AbortJob" %>
<%@ Import Namespace="Shared" %>

<asp:Content ID="HeaderContent" runat="server" ContentPlaceHolderID="HeadContent">
</asp:Content>
<asp:Content ID="BodyContent" runat="server" ContentPlaceHolderID="MainContent"> <h2>Steps</h2>
New Job Created
</asp:Content>
```

## Test file included in highlight.js check in

```cshtml
@model Person

@{
    ViewData["Title"] = "Bootstrap Editors";
}
<div class="overview-form">
    @if(ViewData["Message"] != null) {
        <h3 class="text-success">@ViewData["Message"] </h3>
    }
    else {
        @using(Html.BeginForm(FormMethod.Post)) {
            <div class="form-group">
                @(Html.DevExpress()
                    .BootstrapTextBoxFor(m => m.UserName))
            </div>
            <div class="form-group">
                @(Html.DevExpress()
                    .BootstrapTextBoxFor(m => m.Password)
                    .Password(true))
            </div>
            <div class="form-group">
                @(Html.DevExpress()
                    .BootstrapButton("Register")
                    .Text("Register")
                    .UseSubmitBehavior(true)
                    .SettingsBootstrap(settings => settings.RenderOption(BootstrapRenderOption.Primary))
                    .CssClasses(classes => classes.Control("form-control")))
            </div>
        }
    }
</div>
```
