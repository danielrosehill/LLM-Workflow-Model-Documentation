# Professional GPT Workflows: A Description Of Emerging Best-Practices

*Daniel Rosehill (Overcaffeinated GPT enthusiast)*

![A sloth working with robots in an office](/images/9.webp)

*V1*

**Work in progress!**

What's this, you ask?

A description of *a model* for working with GPT in "professional" context! Or rather: my attempt to explain a workflow model that's *emerging* and which I'm learning to leverage (and thinking of my own spins).

The order is roughly sequential.

## Why I wrote this, who I wrote this for

A lot of people are confused about how and why generative AI has professional application. 

*Isn't ChatGPT just for finding movie recommendations? Isn't DALLE just for maing weird photos of animals? Doesn't it just make sh*t up?*

While there are great books out there like [Prompt Engineering for Generative AI](https://www.oreilly.com/library/view/prompt-engineering-for/9781098153427/), the intention of this repository is to provide a shorter overview of some of the emerging ways in which humans are learning to work seriously with GPTs in professional settings.

## Assumed Prerequisites

Before businesses look into how to use GPT as *effectively* as possible, they've presumably:

- Identified a process which could be enhanced by leveraging generative AI
- Thought about what they would like to achieve by using generative AI
- Dedicated some people to the project and given them some time and latitude to generate valuable outputs from the AI models

All of the above is outside of the scope of this repo and is assumed to be in place.

Once businesses have reached this juncture they may wish to move to:

![Sloth opening GPT system from Amazon](/images/3.webp)

# Step 1: Establishing A System For Managing GPT Work

For the purpose of this repository, let's take "professional" to mean something like:

```
- Approaching the use of GPTs and generative AI tools with a focus on delivering highly focused, optimised, and repeatable outputs
```

There are other signs we could use to delineate between the two (businesses are far more likely to want to use GPTs programatically and to integrate with APIs to extend their usage). 

But this repository is about the *workflow*.

### Prompt Engineering, Custom GPTs

At the time of writing (11-08-24) there are two *primary* methods for improving GPT *outputs* which are widely accessible. Given that GPT 4o subscriptions are available for <$30/month these simple but effective tools are available to countless organisations:

- **Prompt engineering:** The emerging science and art of learning to better leverage existing models
- **Custom GPT development** Harnessing versions of existing GPT models that have been tweaked slightly to focus on a specific *context* or by providing them with additional *knowledge*. 

Both of these efforts are downstream of model creation, training, and improvement. 

![Sloth writing on a huge LLM sign](/images/5.webp)

The *heavy lifting* in AI work entails the development of these large language models (LLMs) developed by tech monoliths which require astronomical amounts of data and computing power to train and develop. But the finishing touches in these individualised configurations can make a huge difference in the utility of the big beasts. 

## Leveraging Prompts & GPTs As Business Assets

Rather than point to a specific "system" *(I'm working on my own project for one; the list of commercial options is markedly scant compared to that of tools focused on generation)* I'm focusing on what the system should *do*. 

If you can set up a relational database and slap together a frontend you could probably build your own prototype in a weekend. GPT technology may be cutting-edge, but for databasing outputs "just CRUD" is good enough. 

Firstly, we're going to be conceive of our prompts and our GPT configurations as digital *assets*. These are the catalysts to better outputs. So if we can develop highly effective assets, we can leverage them to yield tremendous value in the form of superior outputs. By almost anyone's yardstick, that makes them valuable intellectual property (IP). 

As assets, we're going to wish to catalog them meticulously in some kind of database system. We should capture fields like:

```
- Unique ID: The foundation of relational databases. Every "row" gets its own ID.
- Name: For ease of internal reference, let's give our GPT a catchy name
- Purpose
- Version: Capturing a version history is crucial in professional GPT work as we'll be testing and iterating
```

Etc, etc. 

Some tools you could use to quickly kick off this inventory system include:

- Airtable
- NocoDB
- SQLite / MySQL / Postgres + your own system 

You could even set up a private Wordpress site just for this purpose and use the built in taxonomies as the organisational system. 

!([Sloth travelling through space](/images/4.webp)

  ## Separating "Production" & Dev/Staging

  ![/images/6.webp]
  *Professional GPT workflows can entail separate components for "production" and development*

  Consider ChatGPT.

  As a consumer-facing tool, it's intended to be accessed via web UI.

  You come up with a prompt, get an output, and hopefully it's good. If not, you try again.

  ChatGPT can also be used for professional contexts both via its web UI and programatically via its API. 

  Consumers expect regular monthly subscriptions and so the web UI is priced accordingly. 

  By using the ChatGPT API, businesses can use the tool programatically. But there's a catch. Rather than charging a flat monthly fee, OpenAI charges based upon usage. While the upsides of API access are massive, the chance in subscription model introduces a powerful incentive for businesses to be conservative in the generations they run: poorly-written prompts waste both time and money. 

  One other facet of using GPTs programatically is that the *"production"* environment (executing the prompts, gathering and saving the outputs) can be entirely automated. GPT production could simply be a runner on the end of a CI/CD pipeline. 

  ## Staging: Polishing Prompts

![Sloth polishing GPT]([/images/7.webp)

Even if our production process is entirely non-automated, it still makes abundant sense to separate prompt development from prompt production. 

Prompt engineering can be an iterative process and we can focus the vast majority of our intellectual energy here in thinking about how to maximise the effectiveness of the prompts we develop. 

Prompt "production" can be as simple as copying and pasting a well-honed prompt into the ChatGPT UI - or clicking 'run' on a Python script. We then just need to gather the output for analysis. That too can be a separate function. 

## The Simple Data Structure

To bring all the elements together, the following are basic elements in a relational database model capable of tying together all these processes and workflows:

- A custom GPT configuration library for recording the custom GPTs we use
- A prompt lbirary for recording the prompts we have at our disposal
- A GPT workspace where prompt engineers can remain focusd on prompt development
- Some means of capturing prompt output so that it can be leveraged and/or analysed

## The Prompt Workflow Cycle

![[The prompt workflow cycle completes](/images/8.webp)

This version of the cycle could be summarised as follows, broken down step by step.

- We (the business) identifies a process that could be made easier or more effective through leveraging a GPT model
- We may choose to start from the blank slate of the boilerplate model or choose to work some foundational or knowledge into a custom GPT. But either way, we're going to want to develop prompts that can take the *input* of the GPT and deliver the *output* we need to support our business mission
-  We start working on the prompt in our prompt engineering environment. Discrete processes take place here that will be covered later (and added as best practices become clearer). Prompts may be A/B tested, edited, their outputs put through human evaluation panels, and even optimised by GPTs themselves. But finally we're ready to declare that a new *iteration* of the prompt has been reached (or its first).
-  We commit this optimised prompt to our prompt library and make it available to the business user(s). The "user" may actually be a Python script running on a cloud.
-  Our prompt is now in production. The outputs can be captured both for their intended purposes. But also fed back to the prompt development team who can scrutinise the actual outputs against the expected ones and make further changes to optimise the prompt and improve outcomes. The iterative cycle continues.








