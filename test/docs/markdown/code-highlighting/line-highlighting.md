# Line Highlighting

Check out this line highlighting.

<p>When the user selects the <strong>Register</strong> button, the <code>Register</code> action of the Account controller creates the user by calling the ASP.NET Identity API, as highlighted below:</p>
<pre><code class="lang-csharp" name="Main" highlight-lines="8-9">[HttpPost]
[AllowAnonymous]
[ValidateAntiForgeryToken]
public async Task&lt;ActionResult&gt; Register(RegisterViewModel model)
{
    if (ModelState.IsValid)
    {
        var user = new ApplicationUser() { UserName = model.UserName };
        var result = await UserManager.CreateAsync(user, model.Password);
        if (result.Succeeded)
        {
            await SignInAsync(user, isPersistent: false);
            return RedirectToAction(&quot;Index&quot;, &quot;Home&quot;);
        }
        else
        {
            AddErrors(result);
        }
    }

    // If we got this far, something failed, redisplay form
    return View(model);
}
</code></pre>

lorem ipsum

<pre><code class="lang-cshtml" highlight-lines="5-6">@page &quot;/ParentComponent&quot;

&lt;h1&gt;Parent-child example&lt;/h1&gt;

&lt;ChildComponent Title=&quot;Panel Title from Parent&quot;
                OnClick=&quot;@ShowMessage&quot;&gt;
    Content of the child component is supplied
    by the parent component.
&lt;/ChildComponent&gt;

&lt;p&gt;&lt;b&gt;@messageText&lt;/b&gt;&lt;/p&gt;

@code {
    private string messageText;

    private void ShowMessage(UIMouseEventArgs e)
    {
        messageText = &quot;Blaze a new trail with Blazor!&quot;;
    }
}
</code></pre>
<p><em>Components/ChildComponent.razor</em>:</p>
<pre><code class="lang-cshtml" highlight-lines="11-12">&lt;div class=&quot;panel panel-default&quot;&gt;
    &lt;div class=&quot;panel-heading&quot;&gt;@Title&lt;/div&gt;
    &lt;div class=&quot;panel-body&quot;&gt;@ChildContent&lt;/div&gt;

    &lt;button class=&quot;btn btn-primary&quot; @onclick=&quot;@OnClick&quot;&gt;
        Trigger a Parent component method
    &lt;/button&gt;
&lt;/div&gt;

@code {
    [Parameter]
    private string Title { get; set; }

    [Parameter]
    private RenderFragment ChildContent { get; set; }

    [Parameter]
    private EventCallback&lt;UIMouseEventArgs&gt; OnClick { get; set; }
}

</code></pre><h2 id="child-content">Child content</h2>
<p>Components can set the content of another component. The assigning component provides the content between the tags that specify the receiving component. For example, a <code>ParentComponent</code> can provide content for rendering by a Child component by placing the content inside <code>&lt;ChildComponent&gt;</code> tags.</p>
<p><em>Pages/ParentComponent.razor</em>:</p>
<pre><code class="lang-cshtml" highlight-lines="7-8">@page &quot;/ParentComponent&quot;

&lt;h1&gt;Parent-child example&lt;/h1&gt;

&lt;ChildComponent Title=&quot;Panel Title from Parent&quot;
                OnClick=&quot;@ShowMessage&quot;&gt;
    Content of the child component is supplied
    by the parent component.
&lt;/ChildComponent&gt;

&lt;p&gt;&lt;b&gt;@messageText&lt;/b&gt;&lt;/p&gt;

@code {
    private string messageText;

    private void ShowMessage(UIMouseEventArgs e)
    {
        messageText = &quot;Blaze a new trail with Blazor!&quot;;
    }
}
</code></pre>

<pre><code class="lang-cshtml" highlight-lines="1">// Testing boundary conditions. This line should be highlighted and nothing else.

@code {
    private string messageText;

    private void ShowMessage(UIMouseEventArgs e)
    {
        messageText = &quot;Blaze a new trail with Blazor!&quot;;
    }
}
</code></pre>

<pre><code class="lang-cshtml" highlight-lines="10">@code {
    private string messageText;

    private void ShowMessage(UIMouseEventArgs e)
    {
        messageText = &quot;Blaze a new trail with Blazor!&quot;;
    }
}

// Testing boundary conditions. This line should be highlighted and nothing else.
</code></pre>

<pre><code class="lang-cshtml" highlight-lines="4">@code {
    private string messageText;

    // Testing middle boundary conditions. This line should be highlighted and nothing else.

    private void ShowMessage(UIMouseEventArgs e)
    {
        messageText = &quot;Blaze a new trail with Blazor!&quot;;
    }
}
</code></pre>

<pre><code class="lang-cshtml" highlight-lines="1,3,5,7,9,11">// Highlight every other line.

@code {
    private string messageText;

    // Testing middle boundary conditions. This line should be highlighted and nothing else.

    private void ShowMessage(UIMouseEventArgs e)
    {
        messageText = &quot;Blaze a new trail with Blazor!&quot;;
    }
}
</code></pre>

<pre><code class="lang-cshtml" highlight-lines="1,3,5,7,9,11">
// Highlight every other line - blank first line test case.

@code {
    private string messageText;

    // Testing middle boundary conditions. This line should be highlighted and nothing else.

    private void ShowMessage(UIMouseEventArgs e)
    {
        messageText = &quot;Blaze a new trail with Blazor!&quot;;
    }
}
</code></pre>

<pre><code class="lang-cshtml" highlight-lines="1-12">// Highlight everything.

@code {
    private string messageText;

    // Testing middle boundary conditions. This line should be highlighted and nothing else.

    private void ShowMessage(UIMouseEventArgs e)
    {
        messageText = &quot;Blaze a new trail with Blazor!&quot;;
    }
}
</code></pre>