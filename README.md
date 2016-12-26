# Let's Encrypt / Nginx / OpsWorks Chef Recipes

Recipes for custom nginx.conf file generation that supports Let's Encrypt SSL certificate for Rails apps

## 1. You need to edit your App settings to include custom chef recipes

<img width="931" alt="screen shot 2016-12-26 at 17 16 08" src="https://cloud.githubusercontent.com/assets/24574228/21484294/8aaf27fa-cb90-11e6-93ea-30267bc113ed.png">

You need to change 'Use Custom Chef cookbooks' to "Yes"

Put this value as "Repository URL"

```
git@github.com:kodius/kodius-chef-recipes.git
```

So it looks like this:

<img width="982" alt="screen shot 2016-12-26 at 17 16 41" src="https://cloud.githubusercontent.com/assets/24574228/21484295/8ca5d518-cb90-11e6-83ed-2899cc914ec8.png">


For everything to work it is also important to enable "Manage Berkshelf" option, so dependencies will be installed automatically.


## 2. You need to add custom step in App setup

This is added in "Layer Recipes" section

```
kodius-recipes::production_environment
```

It should look like this:

<img width="789" alt="screen shot 2016-12-26 at 18 05 48" src="https://cloud.githubusercontent.com/assets/24574228/21484597/02587aae-cb96-11e6-8a25-b87ad635c0cf.png">
