---
title: "Flight management"
author: Bangyou Zheng
date: '2019-06-15'
slug: meta
weight: 20
tags:
  - meta
output:
  blogdown::html_page:
    toc: false
---


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

