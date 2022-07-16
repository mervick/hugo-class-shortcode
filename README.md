# Hugo class shortcode

Shortcode `class` for hugo is the simplest way to inject classes in the markdown. 


### Usage

Copy [shortcodes/class.html](https://github.com/mervick/hugo-class-shortcode/blob/main/shortcodes/class.html) to your `shortcodes` directory

Add class to custom tag `table`
```md
{{< class tag="table" class="table borderless table-striped" >}}

| Variant | Pulse duration, ns  | Pulse energy, μJ   | Peak power, kW  | Polarization   |
|:--------|:--------------------|:-------------------|:----------------|----------------|
|         | 1.3                 | 100 to 120         | 77 to 92        | Random         |

{{< /class >}}
```

Add class to all tags
```md
{{< class "text-primary" >}}
# header
{{< /class >}}
```

Limit param, to set class only for first table
```md
{{< class tag="table" class="table borderless table-striped" limit=1 >}}

| Variant | Pulse duration, ns  | Pulse energy, μJ   | Peak power, kW  | Polarization   |
|:--------|:--------------------|:-------------------|:----------------|----------------|
|         | 1.3                 | 100 to 120         | 77 to 92        | Random         |

| Variant | Pulse duration, ns  | Pulse energy, μJ   | Peak power, kW  | Polarization   |
|:--------|:--------------------|:-------------------|:----------------|----------------|
|         | 1.3                 | 100 to 120         | 77 to 92        | Random         |

{{< /class >}}
```
