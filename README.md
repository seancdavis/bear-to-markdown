# Bear to Markdown

Export notes within the [Bear](https://bear.app/) application's local database to markdown files.

This project is the output of [this tutorial](https://www.seancdavis.com/posts/export-bear-notes-markdown-files/), which walks through the process of building a Bear exporting tool.

## How it Works

When you run `npm run export`, this is what happens:

1. Bear's database is copied to `database.sqlite` in the root of this project. (Bear stores its content in a local SQLite database, which gets copied so that we don't interfere with the application in any way.)
1. Metadata about the note is converted to YAML frontmatter. The combination of frontmatter and note content is converted to markdown and written to a file in the `tmp/export` directory (within this project).

### Caveats

There are a few caveats to this approach:

- The path to Bear's database is hard-coded in `utils/copyDatabase.js`. You may have to change this.
- You may want to capture different metadata, which is hard-coded in `index.js`.

## Running the Script

If you want to work with this project, first clone the repository:

    git clone git@github.com:seancdavis/seancdavis-com.git

Install dependencies:

    npm install

Run the script:

    npm run export

For more detail on how the code works, [see the tutorial](https://www.seancdavis.com/posts/export-bear-notes-markdown-files/).

## Support

While you could [open an issue](https://github.com/seancdavis/bear-to-markdown/issues/new) in this repository, I'd prefer if you did so [for the tutorial](https://github.com/seancdavis/seancdavis-com/issues/new) instead. (I pay closer attention to the website's repository.) Changes will likely have to be made in both places.

## Contributing

Changes to this example project will likely have to also be made [for the tutorial](https://www.seancdavis.com/posts/export-bear-notes-markdown-files/). If you open a PR here related to the functionality of this project, please also consider making [a relevant change to the post](https://github.com/seancdavis/seancdavis-com/edit/main/www/src/posts/2021-06-16-export-bear-notes-markdown-files.md).

## License

Distributed under my [_Use With Love_](https://www.seancdavis.com/posts/use-with-love-public-license/) license.
