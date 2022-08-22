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

DiscoStream v1.1 in Google Colab [here](https://colab.research.google.com/github/WASasquatch/discostream/blob/dev/DiscoStream.ipynb) 

DiscoStream GitHub Repo Link [here](https://github.com/WASasquatch/discostream)

# Portrait Settings Tips
This is a collection of various suggestions for using the Portrait model. 

## Portrait Model Recommendation
It is currently recommended to utilize portrait_generator_v002

<img width="681" alt="image" src="https://user-images.githubusercontent.com/45181586/186006896-614402f4-120e-4267-9139-ca8e4852a658.png">

## Prompt Writing Recommendations

### Then_SomethingNew Recommendations
I typically recommend structuring prompts the following way with various weights.



```
#General
"a colorful character portrait of a happy ahego kawaii woman wearing cosplay infront of pastel lights,  an anime character portrait by Charlie Bowater and Chris Rallis, featured on deviantart, fantasy art, daz3d, digital painting, digital illustration:3",

#Photography settings
"portrait, center framing, soft focus, cinematic lighting, vertical portrait, f2, 85mm, f1.8, film grain:.75",

#Human Traits
"soft skin, smooth skin, sensual smile, attractive, natural makeup, small nose, kawaii, kawaii woman, cosplay:.5",

#Other Traits
"holography, anamorphic lens flare, luminescence, holographic, cinematic lighting, cosplay, anime:.5",

#Additional Artist References
"by Eric Wallis, by Charlie Bowater, by Daniela Uhlig, by Wlop, by Gil Elvgren, by Rebeca Saray, by Bayard Wu:.25",

#Things to Avoid
"glasses, signature, freckles, blemish, watermark, wrinkles, jpeg artifacts:-1"  
```

# Portrait Settings Links
Then_SomethingNew Examples [here](DiscoStreamSettings/ThenSomethingNewExamples/)

# Helpful Links

# Disco Diffusion Getting Started
