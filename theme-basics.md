# Theme basics

## Creating a new theme

```
hugo new theme mynewtheme
```

## The four "main" templates
* `layouts/_default/baseof.html` Overarching template for everything
* `layouts/_default/list.html` Template for everything that is a list page
* `layouts/_default/single.html` Template for everything that is a content page
* `layouts/index.html` Special template for your front page. Could by skipped if you want it to look like a list or single

### The _baseof.html_ template
{% raw  %}
```html
<!DOCTYPE html>
<html>
    {{- partial "head.html" . -}}
    <body>
        {{- partial "header.html" . -}}
        <div id="content">
        {{- block "main" . }}{{- end }}
        </div>
        {{- partial "footer.html" . -}}
    </body>
</html>
```
{% endraw  %}

## Partials

## Blocks

Blocks are 