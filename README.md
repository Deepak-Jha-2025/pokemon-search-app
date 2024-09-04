# Pokémon Search App

A simple web application that allows users to search for Pokémon by name or ID, retrieving information from the PokéAPI. The app displays various details about the Pokémon, such as its name, ID, type, stats, height, weight, and sprite.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [API Reference](#api-reference)


## Features

- Search for Pokémon by name or ID.
- Display detailed information about the Pokémon, including:
  - Name and ID.
  - Type(s) with corresponding type colors.
  - Base stats (HP, Attack, Defense, Special Attack, Special Defense, Speed).
  - Height and weight.
  - Front sprite of the Pokémon.
- Handles errors gracefully when a Pokémon is not found.
- Responsive design for different screen sizes.

## Technologies Used

- **HTML**: Structure of the web page.
- **CSS**: Styling the web page, including layout and Pokémon type colors.
- **JavaScript (ES6)**: Handles the fetch request, data processing, and DOM manipulation.
- **PokéAPI**: Provides the Pokémon data via a RESTful API.

## Setup and Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/pokemon-search-app.git
    ```
2. Navigate to the project directory:
    ```bash
    cd pokemon-search-app
    ```
3. Open the `index.html` file in your browser to run the app locally.

## Usage

1. Enter the name or ID of a Pokémon in the search bar.
2. Click the "Search" button or press Enter.
3. The app will fetch and display the Pokémon's details, or alert you if the Pokémon is not found.

## Project Structure

```plaintext

pokemon-search-app/
│
├── index.html          # The main HTML file
├── styles.css          # The CSS file for styling
└── script.js           # JavaScript file containing the app logic

```
## API Reference

This app uses the [PokéAPI Proxy](https://pokeapi-proxy.freecodecamp.rocks/) to retrieve Pokémon data.

- **Base URL**: `https://pokeapi-proxy.freecodecamp.rocks/api/pokemon/`
- **Endpoint**: `{pokemonNameOrId}`
  - Replace `{pokemonNameOrId}` with the name or ID of the Pokémon you want to fetch (e.g., `pikachu`, `25`).

### Example API Request

```bash
https://pokeapi-proxy.freecodecamp.rocks/api/pokemon/pikachu
```

### Example API Response

```bash
{
  "id": 25,
  "name": "pikachu",
  "height": 4,
  "weight": 60,
  "sprites": {
    "front_default": "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/25.png"
  },
  "stats": [
    { "base_stat": 35, "stat": { "name": "hp" } },
    { "base_stat": 55, "stat": { "name": "attack" } },
    { "base_stat": 40, "stat": { "name": "defense" } },
    { "base_stat": 50, "stat": { "name": "special-attack" } },
    { "base_stat": 50, "stat": { "name": "special-defense" } },
    { "base_stat": 90, "stat": { "name": "speed" } }
  ],
  "types": [
    { "slot": 1, "type": { "name": "electric" } }
  ]
}
```
