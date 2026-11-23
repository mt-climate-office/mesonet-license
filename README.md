# Montana Mesonet data license

All Montana Mesonet data are licensed under
[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
Anyone can copy, share, and adapt them, including commercially, as long as
they credit the Montana Mesonet. The legal code is in [`LICENSE`](LICENSE).

This repository holds the license, the exact wording that every Mesonet
product uses, and the list of places where that wording appears.

## What the license covers

The license applies to data the Montana Climate Office measures at Montana
Mesonet stations, from every place they are published:

- Observations, at every QC level, from the
  [Mesonet API](https://mesonet.climate.umt.edu/api/v2/docs), the OGC API,
  and the [data archive](https://data2.climate.umt.edu/mesonet/data/)
- Logger source records (`data2.climate.umt.edu/mesonet/loggers/`)
- Station camera photos (`…/mesonet/photos/`)
- Station power data (`…/mesonet/power/`)
- Station compliance summaries (`…/mesonet/compliance/`)
- Soil water retention data (`…/mesonet/soils/`)

**Not covered:**

- **Air quality** (`…/mesonet/air-quality/`). These are PurpleAir sensor
  readings fetched through PurpleAir's API. They stay out of scope until
  PurpleAir's terms have been reviewed.
- Software. Each code repository carries its own license.
- Other Montana Climate Office data products (drought indices, gridded
  climate data, normals, and so on). They are licensed separately.

The [user agreement and disclaimer](https://climate.umt.edu/about/agreement/)
also applies. It disclaims warranties and adds no restriction on use.

## How to credit the data

### Short statement

> Montana Mesonet data are licensed under CC BY 4.0. Credit: Montana Mesonet,
> Montana Climate Office. A service of the University of Montana.

### Full citation

> Montana Mesonet, Montana Climate Office. A service of the University of
> Montana. {Year Accessed}. Data accessed from {URL} on {Access Date}.
> Licensed CC BY 4.0.

To cite a fixed snapshot of the data archive, use the archive citation
instead. It is in the
[archive README](https://data2.climate.umt.edu/mesonet/data/README.md).

### Short in-text credit (dashboards, figures, apps)

> [Data from the Montana Mesonet](https://climate.umt.edu/mesonet/citation/),
> a service of the University of Montana ·
> [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

The first link goes to the full citation. CC BY 4.0 §3(a)(2) allows credit to
be given through a link to a page that contains it. Keep "CC BY 4.0" visible
next to the credit; do not leave it only on the linked page.

HTML:

```html
<a href="https://climate.umt.edu/mesonet/citation/">Data from the Montana Mesonet</a>,
a service of the University of Montana ·
<a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>
```

Markdown:

```markdown
[Data from the Montana Mesonet](https://climate.umt.edu/mesonet/citation/), a service of the University of Montana · [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
```

Plain text, where links don't work (a printed figure, for example):

```text
Data: Montana Mesonet, a service of the University of Montana. CC BY 4.0.
```

## Where the license is stated

When Mesonet data are published somewhere new, add that place to this table
and copy the wording above.

| Surface | Repository | File |
|---|---|---|
| User agreement (`climate.umt.edu/about/agreement/`) | mco-website, mco-website-next | `_pages/about/about_agreement.md`; `src/pages/about/agreement.astro` |
| Mesonet citation (`climate.umt.edu/mesonet/citation/`) | mco-website, mco-website-next | `_pages/mesonet_citation.md`; `src/pages/mesonet/index.astro` (`#mesonet-cite`) |
| Mesonet API, `mesonet2.climate.umt.edu/api/v2` | mesonet-db-rds | `api/app/app/main.py` (`license_info`) |
| Mesonet API, legacy `mesonet.climate.umt.edu/api/v2` | mesonet_app | `apiv2/app/app/main.py` (`license_info`) |
| OGC API – Features | mesonet-ogc | `pygeoapi-config.yml` (`license`) |
| data2 root (`/mesonet/`) | mco-aws | `stacks/mco-mesonet-bucket/public/README.md` |
| data2 archive (`/mesonet/data/`) | mesonet-db-rds | `docs/archive-public-README.md` |
| data2 loggers (`/mesonet/loggers/`) | mesonet-loggernet | `publish/README.loggers.md` |
| data2 photos (`/mesonet/photos/`) | mesonet-cameras | `src/mesonet_cameras/assets/README.photos.md` |
| data2 power (`/mesonet/power/`) | mesonet-power | `src/mesonet_power/PUBLIC_README.md` |
| data2 compliance (`/mesonet/compliance/`) | mesonet-compliance | `public/README.md` |
| data2 soils (`/mesonet/soils/`) | mesonet-soils | `LICENSE`, `CITATION.cff`, `README.md` |
| data2 air quality (`/mesonet/air-quality/`): **excluded**, noted as such | mesonet-aq | `src/mesonet_aq/PUBLIC_README.md` |
| Dashboard data manifest (soils entry) | mesonet-dashboard | `web/src/core/ag/data/vendor-static.mjs` |

Questions: state.climatologist@umontana.edu
