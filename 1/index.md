# Tech Docs

Tech Docs is a project borne out of a lack of simple and easy to use software for documentation.

## Getting started
To get started you need to set up a new project. Tech docs is built as a composer project.

To get started you'll need to have composer set up and then run:

`composer create-project that-chris-r/docs <DIRECTORY NAME>`

Once the project is cloned you should edit `app/config.php` and set the global view variables based on your projects needs.

You then should set up the configuration for documentation. Tech docs is designed to host multiple projects documentation. To define the documentation you edit `app/Routes.php` and then add an array to the add_routes function call.

```
Router::add_routes(
    [
        'techdocs' => [
            'versions' => true
        ]
    ]
);
```

For full configuration options [see here](configuration/index).

Once you have set up your project you can start writing your documentation, it will sit inside the docs folder and the folder structure will match the url structure on the front end of the application. E.G. This page is at `/techdocs/1/index` which means that it is actually sitting at `/docs/techdocs/1/index.md`

### Markdown

Markdown is a simple to use language that gives you certain flexibility without needing to use a more complex language such as HTML.

Tech docs is built around using markdown files as a source.