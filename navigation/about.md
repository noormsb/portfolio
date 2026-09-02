---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

Here are my favorite states in America that I've been to before.

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Homebase", "description": "California - 2014"},
        {"flag": "f/f1/Flag_of_Nevada.svg", "greeting": "Vegas", "description": "Nevada - 2020"},
        {"flag": "5/54/Flag_of_Washington.svg", "greeting": "Almost Canada", "description": "Washington - 2026"},
        {"flag": "e/e6/Flag_of_Alaska.svg", "greeting": "The Final Frontier", "description": "Alaska - 2024"},
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### What I Did In These Places

Here's what I got up to in each state.

- 🏔️ California — I've lived in San Diego for 12 years. It's home, and it's also where most of my hiking happens — I love the local trails, plus trips to Yosemite and Kings Canyon National Parks.
- 🎰 Nevada — Went to Las Vegas, saw Hoover Dam up close, and spent time at Lake Tahoe.
- 🌲 Washington — Hiked Mt. Rainier National Park, explored more of the state's national parks, and checked out Seattle, including the Space Needle.
- 🧊 Alaska — My favorite trip so far. Visited Denali and Kenai Fjords National Parks, took a cruise past glaciers, and landed on top of a glacier by helicopter.

### What's Important to Me

- 🕌 My faith — I'm Muslim, and it's a big part of who I am.
- 👨‍👩‍👦 My family — my mom, dad, and older brother.
- 🐱 My cat, Rumi. I had another cat, Emy, who passed away two years ago.
- 🧪 My favorite subjects are math and science, especially chemistry — I'm aiming to become an electrical engineer.
- ♟️ My hobbies: chess, hiking, riding my mountain bike and my electric dirt bike, and video games.

<comment>
Gallery of Pics, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="{{site.baseurl}}/images/about/creek.jpeg" alt="Image 1">
  <img src="{{site.baseurl}}/images/about/green.jpeg" alt="Image 2">
  <img src="{{site.baseurl}}/images/about/rumi1.JPG" alt="Image 3">
  <img src="{{site.baseurl}}/images/about/bike.jpeg" alt="Image 4">
  <img src="{{site.baseurl}}/images/about/rumi2.jpeg" alt="Image 5">
  <img src="{{site.baseurl}}/images/about/uphill.jpeg" alt="Image 6">
</div>