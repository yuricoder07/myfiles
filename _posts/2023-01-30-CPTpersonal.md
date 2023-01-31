---
toc: true
layout: post
description: overview of my CPT project
categories: [markdown]
title: CPT overview
---

# Overview
For our group CPT project, we are doing a recipe suggester. We called our project reciPies. My share for the project is to create a favoriting system where a user who is logged in can favorite a recipe. This will allow them to see it again if they ever wanted to.

## Purpose and Function
Purpose: allows a user who is logged in to favorite recipes they like so they can come back.

​Function: There will be a frontend that allows a user to click a grey star. Once the star is clicked, the start will turn gold. When the user clicks the star it will save in a database linking to the logged on users account, that will have a table of saved recipes.

## Data Abstraction
When the JSON data for all the saved recipes is parsed, then a list called userfavorites, will record all of the favorited recipes. This will recorded on a frontend table on the website.


## Managing Complexity
Using a list called userfavorites it allows managing complexity because it allows the program to easily access the user favorites and append to a frontend table.


## Procedural Abstraction
A procedure, called addFavorite(), would allow a user to add a favorite, appending it into the JSON list. I can also have a procedure called accessStorage() allowing it to access the data stored in the JSON file, and converting it to a format that I can use to code.


## Algorithm Implementation

Sequencing will be used in order to sort the most recently added favorite recipe to the oldest recipe on the bottom. This is important because users can get a sense of time of how long ago they favorited the recipe.


## Testing
My two tests would be with a review of the favorited recipes in the JSON list:
1. Test to see if when clicked the favorited recipe is added to the JSON list 
2. Test the accessStorage() function to see if I'm able to access the stored favorited data.

## Video Plan

I will show the input(clicking the button), reload the page and show how it saves. I will then go on the backend showing the JSON db with the stored feilds. After that I will go to the table page (frontend) which shows all the stored favorited recipes.

