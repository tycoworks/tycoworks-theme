# tycoworks-theme

The tycoworks slide theme for [tycoslide](https://github.com/tycoworks/tycoslide).

```bash
npm install
npx tycoslide build showcase.md   # 21 slides covering all 18 layouts
```

## Contents

```
template/tycoworks-demo.pptx   the design; tycoslide fills it, never edits it
theme.json                     the map onto it
assets/                        icons, brand marks, backdrops
assets.json                    the catalog of those images
showcase.md                    a deck exercising every layout
```

`npx tycoslide package` builds the Agent Skill, `tycoworks-theme.zip`, whose
`manifest.json` lists every layout's name, parameters and slots.

## Design

Eighteen layouts. Title, Section and Closing are dark; the rest are light.

Type is Inter, with Fira Code for code, both embedded in the template.

Color lives in the template's theme rather than `theme.json`, so change a
scheme slot rather than painting shapes:

| Slot | Value | Role |
| --- | --- | --- |
| `lt1` | `#1A1A2E` | body type on light; ground on dark |
| `dk1` | `#FFFFFF` | ground on light; type on dark |
| `dk2` | `#7C3AED` | accent type, icons, rules |
| `lt2` | `#EDE9FE` | tinted surfaces — stat boxes, table headers |

## Icons

`assets/icons/` holds 2,122 icons: the complete filled style of
[Material Icons](https://fonts.google.com/icons), from
`@material-design-icons/svg@0.14.15`, rasterized to 96px and tinted
`#7C3AED`. Retint them by overwriting RGB and preserving alpha; they are
monochrome masks.

Catalog descriptions are Google's own keyword tags, trimmed to six terms, so
`assets.json` is searchable by concept. Search it rather than reading it.
