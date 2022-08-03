---
layout: post
title: Make a Texture manager with pygame!
---

Loading textures in pygame can be hard and boring. So, today I will show you how to automatically load textures! Every texture works as soon as you save it

from your paint app. Let's get started.


### Initial Setup

1. Firstly, we will need to import some libraries. Import:
  import pygame
  import os
  
2.Get the working directory:
 cwd = os.getcwd()
 
3. Make a GLOBAL Texture List `TEXTURE_LIST = {}`
 
### The Texture Loader
1. First things first, we'll need to make a function that reads the files `def get_files(folder):`

	def get_files(fold):
		res = []

		for path in os.listdir(fold):
		    if os.path.isfile(os.path.join(fold, path)):
		        res.append(path)
		return res
