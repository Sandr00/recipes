# Recipes

[![Build Status](https://travis-ci.com/Sandr0x00/recipes.svg?branch=master)](https://travis-ci.com/Sandr0x00/recipes)

## What is this

Just a small website based recipe collection for me.

## How does it look

Check out the live version at [https://sandr0.tk/recipes/](https://sandr0.tk/recipes/)

## How can I use it

Clone/fork this rep.

Create `config.json` next to `server.js`:

```json
{
  "port": 8082
}
```

Run:

```bash
npm install
npm run build
npm run start
```

Deploy (still manually):

```bash
npm run zip
# copy recipes.tar.gz to your server and extract it there, everything now on server
npm install --production
./server
```

## How can I add recipes

Recipe

- Add &lt;name&gt;.json to recipes.
- It has to contain the following fields:

```json
{
  "name": "<The name of your recipe>",
  "portions": "<optional>",
  "tags": ["<tag1>", "<tag2>", ],
  "ingredients": [
    {
      "id": "<id, Used for preparation. If a recipe with that id exists, it will automatically get linked>",
      "amount": "<optional>",
      "name": "<name which is displayed>"
    },
    {
    }
  ],
  "preparation": ["<first step>", "<second step>", ]
}
```

- It is possible to link ingredients in your preparation by using `{id}` or `{id:amount}` in preparation. Example: You have an ingredient with `"id": "salt"`. Now you can use `{salt}` in preparation.

## Contribution

Feel free to give me a PR (or write me at Twitter: [@Sandr0x00](https://twitter.com/Sandr0x00)), if you got a nice recipe, or want to improve the code. I always try new stuff. I kind of think,someday I will be a better cook than programmer.

Currently, all recipes are written in german, but maybe someday, someone will translate them :)

## Author

[Sandro Bauer](https://twitter.com/Sandr0x00)
