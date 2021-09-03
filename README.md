# Climate Change Infographics Repository

This repository contains all of the infographics and their associated metadata. An infographic and its metadata are together called an 'item'.

## Structure

### `tags.yml`

Contains a list of tags that can be applied to items.

### `categories.yml`

Contains a list of categories. Categories are essentially a name for a bundle of 'tags' and/or of individual items.

### `items/`

All items can be found in this directory.

They can be organised into subdirectories, each subdirectory optionally applying metadata to all of the items and/or directories contained within it by setting these options in `config.yml`.

An item has the following structure and is uniquely identified by its path inside the `items/` directory:
- `[item_name].(png|jpeg|svg)`
- `[item_name].yml`

## Item/Subdirectory configuration options

The following fields are available to be set on each item or subdirectory (sometimes) config:

| Name | Description | Subdirectory Enabled |
| ---- | ----------- | -------------------- |
| title | The title of the item. | ❌ |
| description | Markdown-enabled description of the item. | ✔️ |
| authors | List of `Author`s of the item. | ✔️ |
| source | `Source` of the item. | ✔️ |
| publication_date | `yyyy-mm-dd` formatted date of the publication of this item at the source. | ✔️ |
| license | An absolute URL to the license document. | ✔️ |

For all of the Subdirectory-Enabled options, the keyword `!INHERIT` may be used to inherit any settings from parent configurations, to be extended.

### Author

Can either be a simple string, in which case it is interpreted as the author's name, or an object with the fields:

| name | description |
| ---- | ----------- |
| name | The name of the author. |
| url | URL of the authors home page. |

NB: In future, a centralised author catalogue may be implemented.

### Source

An object with the fields:

| name | description |
| ---- | ----------- |
| name | The name of the author. |
| url | URL of the authors home page. |
| date_retreived | `yyyy-mm-dd` formatted date of when the item was retreived from this source. |

NB: In future, a centralised author catalogue may be implemented.