# Introduction
This is a Hands On project created for the TECAA course by Cristóvão Sampaio, Hugo Silva, João Oliveira and Marta Ribeiro.

# Prerequisites
- Clone of repository: [HandsOnGithub](https://github.com/martamribeiro/TECAA_HandsOn)

# TECAA HandsOn tasks
Navigate to the "InitialProject" folder, as this folder will be the one you shall use to complete these tasks. In "FinalProject" you will find a complete version of the project, or in other words, an example project of how you Hugo/Doks website should look like by the end of this Hands On.

## 1- Install Dependencies and Start the Development Server
Navigate to the "InitialProject" folder. While inside this directory, open the command line and install the dependencies before continuing.
``` bash
npm install
```

When working locally, [Hugo’s development server](https://gohugo.io/commands/hugo_server/) lets you preview your work and automatically refreshes your browser when you make changes.

Inside the same directory as before, run the following command to start the development server:
| npm | pnpm | Yarn |
| :----: | :----: | :----: |
| ``` npm run dev``` | ``` pnpm dev``` | ``` yarn dev``` |

This will log a message to your terminal with the URL of your local preview, just like the command ``` hugo server``` does.

## 2- Add a Link Card from the "The End" documentation page
Navigate to the example.md file found inside content/docs/end in the "InitialProject" folder. There, you can create a Link Card that sends us to a secret page by using the following code:

``` bash
{{< link-card
  title="Secret Page"
  description=""
  href="/random/"
>}}
```

You should now save the changes and see the results for yourself.

## 3- Add two Link Cards (with Card Grid) to the newfound page
Now, find the _index.md associated with the /random/ page. There, you can create a Card Grid that allows you to stack horizontally two Link Cards. This can be achieved by inserting the following code:

``` bash
{{< card-grid >}}
  {{< link-card
    title="Docs"
    description="Go back to the Docs"
    href="/docs/end/the-end/"
  >}}
  {{< link-card
    title="Docs"
    description="Go back to the Docs"
    href="/docs/end/the-end/"
  >}}
{{< /card-grid >}}
```

You should now save the changes and see the results for yourself.

As you might have noticed, both Link Cards send the user to the same webpage. Now, make it so that the grid showcases one Link Card to the Docs page and another to the Blogs page, using the code below:

``` bash
  {{< link-card
    title="Blog"
    description="Explore the Blog page"
    href="/blog/"
    target="_blank"
  >}}
```

The inserted code has a "target" attribute defined. Can you still remember what it is used for? :D