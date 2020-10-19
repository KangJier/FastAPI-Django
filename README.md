# FastAPI-Djando
Using FastAPI with Django
# Introduction
The code  
Without further delay, the part you’ve all been waiting for, the code. This section includes both the bare essentials for getting the integration working, and some best practices I’ve found when working with FastAPI, such as URL reversing, easier DB model to API model conversion, etc. I hope you’ll find it useful.
Starting out
To begin, install FastAPI, Uvicorn and Django and create a Django project as you normally would. I recommend my “new project” template, it contains various niceties you may want to use. We’re going to replace some parts and add others. I’ve created a project called goatfish and an app called main to illustrate, you can call yours whatever you want. Make sure you add "main" to Django’s INSTALLED_APPS list in the settings so it discovers the models and migrations.
The models  
We should probably start with our data model so everything else makes sense. The API is going to be a straightforward CRUD API, which will serve a model we’ll call Simulation and provide authentication.  
Since we have an API and a database, and the models for the two are neither semantically nor functionally identical, we’ll have two sections in our models.py, one for each model type.