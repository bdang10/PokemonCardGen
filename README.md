# Pokemon Card AI Generator

This Python script will use natural language processing AI to create new and custom Pokemon cards.

It will use OpenAI to generate a Pokemon name and a description, and creates
a prompt for [Midjourney](https://midjourney.com/home) (which needs to be used manually).

Then a separate command can be used to combine the Pokemon data with the generated artwork to create a new Pokemon card.

The output will be in the `/output` folder, with empty folders for you to put card artwork into.

```
[project root]
├───output
    ├───cards
    ├───images
```

The cards will have JSON like this:

```json
{
  "index": 26,
  "name": "Flamo",
  "description": "...",
  "element": "Fire",
  "rarity": "common",
  "rarity_index": 0,
  "hp": 50,
  "abilities": [
    {
      "name": "Scorch",
      "element": "Fire",
      "cost": 2,
      "is_mixed_element": false,
      "power": 40
    }
  ],
  "image_prompt": "a chibi young fire-type parrot pokemon, in a volcano environment, lava texture background, anime chibi drawing style, pastel background --niji --ar 3:2",
  "image_file": "026_flamo.png"
}
```

You can use the `image_prompt` to generate the card artwork with Midjourney.

# Setup

1. Install Python 3.10 (or higher)
2. Install the dependencies with `pip install -r requirements.txt`
3. Set your PYTHONPATH to the `src` so that the modules can be imported.

   ```bash
   # For bash, you can use:
   export PYTHONPATH=$PYTHONPATH:src
   ```
