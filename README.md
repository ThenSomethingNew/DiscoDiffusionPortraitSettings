# Disco Diffusion Portrait Settings

A collection of settings, tips, tricks, and resources for creating artistic portraits with Disco Diffusion

<img width="944" alt="image" src="https://user-images.githubusercontent.com/45181586/185998497-9bca8ace-7605-4c00-8f73-028932fa2168.png">

[@then_somethingAI](https://www.instagram.com/then_somethingai/) on Instagram


# Table of Contents
Getting Started with Disco Stream (assumes general knowledge of Disco Diffusion) 
[here](#disco-stream-getting-started)

Portrait Settings Tips & Tricks
[here](#portrait-settings-tips)

Portrait Settings Links (to other examples in the GitHub repo)
[here](#portrait-settings-links)

Other Helpful Links 
[here](#helpful-links)

Getting Started with Disco Diffusion (for new users to Disco Diffusion) 
[here](#disco-diffusion-getting-started)

Contact [Join our Discord](https://discord.gg/HNDPwD9T)

# Disco Stream Getting Started
It is highly recommended to utilize the DiscoStream fork of DiscoDiffusion [@WAS](https://github.com/WASasquatch) has done a great job of integrating custom features to help facilitate using new and experimental models (including using the Portrait Model)

*this guide assumes a basic understanding of using DiscoDiffusion in Google Colab*

DiscoStream v1.1 in Google Colab [here](https://colab.research.google.com/github/WASasquatch/discostream/blob/dev/DiscoStream.ipynb) 

DiscoStream GitHub Repo Link [here](https://github.com/WASasquatch/discostream)

# Portrait Settings Tips
This is a collection of various suggestions for using the Portrait model. This section uses this image as an example to what settings were modified to create the following result. *these settings are based on a V100 allocation in Google Colab and may run out of memory on a free T4*

<img width="282" alt="image" src="https://user-images.githubusercontent.com/45181586/186010433-a30a7e75-39f4-4597-8d90-1feb7ade76d3.png">

## Clip Models
These are the current recommended clip models to use for Portrait images

<img width="189" alt="image" src="https://user-images.githubusercontent.com/45181586/186011333-3649bdd1-3e58-45af-bf76-71c2415a992d.png">

## Portrait Model Recommendations 
It is currently recommended to utilize portrait_generator_v002

<img width="681" alt="image" src="https://user-images.githubusercontent.com/45181586/186006896-614402f4-120e-4267-9139-ca8e4852a658.png">

## Settings Recommendations
These settings deviate from the initial recommendations from @Felipe3DArtist to create more wild and creative results using a higher clamp and step count to attempt to find a sweet spot between referencing the initial dataset and coming up with something new. 

## Initial Settings

<img width="464" alt="image" src="https://user-images.githubusercontent.com/45181586/186011557-44c73a53-9dec-419c-a99d-f8d19b1f5b4e.png">

**Width / Height** recommended for tall posts on instagram (the recommended dimensions against the initial model of 512x512 will produce more stable results)

**Clip Guidance Scale** Play around and experiment high numbers (20-30k) produce more creative resultes, (8k-15k) is a good mid range, (less than 5k) produce more photorealism

**TV,RANGE,SAT Scale** More creative and saturated results the higher you go, reduce these to get more photo realism

**Cutn Batches** 4 is a good sweet spot for more creative results, if you are running on a T4 consider reducing this to 1 to save on memory

## Cut Scheduling
This is where the majority of the work comes into play asside from settings and prompts. Play with these, have a laugh see what works out for you. However, this can be a good starting point.

<img width="500" alt="image" src="https://user-images.githubusercontent.com/45181586/186012599-9c50b70e-a555-4080-8788-f63b9fe79f79.png">

**Cut_overview** Starts big and goes down to 0. This structures the overall composition of your image before tapering off. 

**Cut_innercut** Starts at nothing and increases in the middle before tapering off again. Play with options to give it a few innercuts at the beginning for more detail later in the image or try something completely different

**Cut_ic_pow** Still a WIP and playing around, but current strategy has a higher power at the beginning to form initial shapes, tapers down to add in detail, ramps up for detail, and turns down again at the end so the overall image doesn't get to grainy

**Cut_icgray** Starts small and tapers off so the initial diffuse steps focus on geometry


## Prompt Writing Recommendations

**Remember the Prompt isn't everything**
In fact it's just a part of your overall settings. However, good results have been found with the portrait model by breaking up and grouping similar image prompt information together rather than one long sentence. 

*things to note*
The sum of the prompt weights > 1
It helps to use the same word in singular and plural (mirror, mirrors...)

```
#General
"a bright illuminated painting of a woman with purple hair breaking through reflective mirrors, a character portrait by Charlie Bowater and Chris Rallis, featured on deviantart, fantasy art, daz3d, digital painting, digital illustration:3",

#Photography settings
"portrait, center framing, soft focus, cinematic lighting, vertical portrait, f2, 85mm, f1.8, film grain:.75",

#Human Traits
"soft skin, smooth skin, sensual smile, attractive, natural makeup, small nose, long beautiful hair:.5",

#Other Traits
"holography, anamorphic lens flare, luminescence, holographic, mirrors, mirror, broken mirror, broken glass, shattered mirror, mirrors:.5",

#Additional Artist References
"by Eric Wallis, by Charlie Bowater, by Daniela Uhlig, by Wlop, by Gil Elvgren, by Rebeca Saray, by Bayard Wu:.25",

#Things to Avoid
"glasses, signature, freckles, blemish, watermark, wrinkles, jpeg artifacts:-1"  
```

# Portrait Settings Links
Then_SomethingNew Examples [here](DiscoStreamSettings/ThenSomethingNewExamples/)

# Helpful Links

# Disco Diffusion Getting Started
