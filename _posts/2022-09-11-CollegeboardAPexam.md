---
toc: true
layout: post
description: Performance Task Plan
categories: [markdown]
title: Collegeboard AP Exam Plan
---

# Idea 1

## Performance Task/Program Purpose and Function

For my APCSP project, I want to make an program that requests from blockchain APIs, and find if a transaction has confirmed towards a certain bitcoin address

The user will be able to input a bitcoin address or a TXID(transaction hash) into the program for the results.

## Data Abstraction

In this program the data requested by the API's will be stored in a dictionary. The program will access the data in the lists and dictionaries, and run them through functions that check if the transaction confirmed or is unconfirmed. The program will also store data about the transaction like fees, and dates on when the transaction was initiated.


## Managing Complexity

This is still being thought out, but the main idea is to ideitify information based on a transation using the blockchain. It will output data like the transaction fees, and how long it takes or took the transaction to confirm on the blockchain.

## Procedural Abstraction

The procedure for this program is to first take a TXID input by the user, then to request from blockchain APIs about the transaction. The API responses are then saved in a dictionary that are extracted and formated for the user to interpret.

## Algorithm Implementation

The algorithm implementation would have to do with parsing/iterating the data saved in the dictionary. My program would need to assosiate variables with certain data. The Algorithm would need to loop through the data to output the right information the user.

## Testing

For the testing, I will demonstrate how to use the program through a short video. I will also include a written documentation that explains how the program works as well as how to use it.

