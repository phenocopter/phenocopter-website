---
title: "Meta management"
author: Bangyou Zheng
date: 2020-07-15
slug: meta
weight: 20
tags:
  - meta
toc: true
menu:
  docs:
    parent: introduction
    weight: 3
---


## Meta Structure

In the PhenoCopter, three levels of structure are used to manage all flights, i.e. *Farm*, *Field*, *Flight*.

* *Farm* belongs to each user and is the root folder to manage flight.
As the folder structure in the backend storage, the farm name has to be unique for all users.
* *Field* refers to each experiment block in a farm. A timeline is available for all flights in a field.
* *Flight* refers to the actual flight.

{{% alert theme="danger" %}}
The names of farm, field and flight cannot be changed as we use them after creating as the folder name. You have to carefully choice them.
{{% /alert %}}


{{% alert theme="danger" %}}
The farm name has to be unique in the whole system, even you don't use it. A better practice is to add a prefix in your farm name.
{{% /alert %}}


## Permission

The farm owner has read and write permission to manage all fields and flights in a farm and shares with other users with write or read permission. The permission can be created and retrieved separately to farm, field and flight. The owner also can set a flight as public which are viewable for any users. 

A **Share** button can be found in the list of farm, field and flight to share with other users in the system.

## Create a new farm

A new farm can be created in the page of *Farm* list. Just click the 
button `New Farm`, then type a `new name` and `note`,
finally click `Submit` button.

## Create a new field
A new field can be created in the page of *Field* list. Just click the button `New Field`, then select a `farm` from list, 
type a `field name` and  `note`, finally click the `Submit` button. 

You can type to search the farm name in the list.

## Create a new flight

