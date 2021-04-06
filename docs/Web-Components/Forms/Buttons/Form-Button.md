# Form Button

Renders a button including form-tag. Works best with named routes. Can be used inline as default link element.

## Bare

The bare or renderless component has no styles. Perfect to use it inline. This simple example

```blade
<x-form-button :action="route('login')">
    Login
</x-form-button>
```

will render

```html
<form method="POST" action="https://tallui.io/login">
    <input type="hidden" name="_token" value="...">
    <input type="hidden" name="_method" value="POST">

    <button type="submit">
        Sign Out
    </button>
</form>
```

View component: [https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#bare](https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#bare)

## Methods

Using different HTTP-methods

```blade
<x-form-button 
    :action="route('page', $pid)"
    method="DELETE"
>
    Delete
</x-form-button>
```

will render

```html
<form method="POST" action="https://tallui.io/pages/1337">
    <input type="hidden" name="_token" value="...">
    <input type="hidden" name="_method" value="DELETE">

    <button type="submit">
        Delete
    </button>
</form>
```

## Style

Use TallUI directives to style your components the easiest way possible.

```blade
<x-form-button :action="route('login')" tui="full lg success stroke">
	Sign In
</x-form-button>
```

will render

```html
<form method="POST" action="https://tallui.io/login">
    <input type="hidden" name="_token" value="...">
    <input type="hidden" name="_method" value="POST">

    <button type="submit" class="btn-lg btn-full success stroke">
        Sign Out
    </button>
</form>
```

View component: [https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#style](https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#style)

### Width

- default (default)
- full

### Size

- sm
- md (default)
- lg

### Color

- primary (default)
- secondary
- muted
- transparent
- success
- warning
- danger
- cta
- grey
- black
- white

### Style

- rounded
- fill (default)
- stroke

## Disabled

The simplest disabled-button looks like this:

```blade
<x-form-button :action="route('update')" tui="disabled">
	Please wait ...
</x-form-button>
```

will render

```html
<form method="POST" action="https://tallui.io/update">
    <input type="hidden" name="_token" value="...">
    <input type="hidden" name="_method" value="POST">

    <button type="submit" class="button muted" disabled>
        Please wait ...
    </button>
</form>
```

View component: [https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#disabled](https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#disabled)

## Icon

## Icon with text

## Animated Icon

## Dark-Theme

If Dark-Theme is not enabled by default, you can [enable Dark-Theme](https://tallui.io/docs/alpha/theme/configuration#dark-theme) in your theme configuration. TallUI automatically adds dark-theme classes to all components. If you need to override the dark-theme settings, you can:

```blade
<x-form-button :action="route('login')" tui="lg full success animate-xxx">
	Sign In
</x-form-button>
```

will render

```html
<form method="POST" action="https://tallui.io/login">
    <input type="hidden" name="_token" value="...">
    <input type="hidden" name="_method" value="POST">

    <button type="submit" class="button" class="btn-lg btn-full color-success">
        Sign Out
    </button>
</form>
```

View component: [https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#dark](https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#dark)

## Animation

If Animation is not enabled by default, you can [enable Animation](https://tallui.io/docs/alpha/theme/configuration#animation) in your theme configuration. The defaults might already fit your needs, if not:

```blade
<x-form-button :action="route('login')" tui="lg full success animate-xxx">
	Sign In
</x-form-button>
```

will render

```html
<form method="POST" action="https://tallui.io/login">
    <input type="hidden" name="_token" value="...">
    <input type="hidden" name="_method" value="POST">

    <button type="submit" class="button" class="btn-lg btn-full color-success">
        Sign Out
    </button>
</form>
```

View component: [https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#animation](https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#animation)

## Scroll animation

If Scroll animation is not enabled by default, you can [enable Scroll animation](https://tallui.io/docs/alpha/theme/configuration#scroll-animation) in your theme configuration. The defaults might already fit your needs, if not:

```blade
<x-form-button :action="route('login')" tui="lg full success scroll-xxx">
	Sign In
</x-form-button>
```

will render

```html
<form method="POST" action="https://tallui.io/login">
    <input type="hidden" name="_token" value="...">
    <input type="hidden" name="_method" value="POST">

    <button type="submit" class="button" class="btn-lg btn-full color-success">
        Sign Out
    </button>
</form>
```

View component: [https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#scroll](https://tallui.io/docs/Web-Components/Forms/Buttons/Form-Button#scroll)

## Mix and extend

Add your own things. Add few rules and don't forget to purge to production. Keep it small, please.

```blade
<x-form-button :action="route('login')" tui="large full" class="bg-blue-500">
	Sign In
</x-form-button>
```
