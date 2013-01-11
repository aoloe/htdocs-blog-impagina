---
title: Small tools rule the world
---
For several years now, I've been following the [Suckless mailing list](): a very inspiring place, if you can live with the fact that it's a rather rude place...

Today I was reading Damien Katz longer article on [The Unreasonable Effectiveness of C](damienkatz.net/2013/01/the_unreasonable_effectiveness_of_c.html). It's not that I would be fond to create anything in C. I don't know why, but it does not sound that appealing to me. But it makes me open my eyes on the fact that using a language or framework that helps you manage the complexity is not always the good answer. More often than you think, you'd better try to avoid the complexity itself. As an example by splitting the problem in parts that are easier to manage.

The core problem bein the layers of abstraction? Many people, seem to value the difficulties to debug failures accross them, but from the perspective of a Scribus developer, the biggest hurd seems to be in the hard time you have each time you dive into a piece of code.

One idea is to produce lot of small – highly specific – tools and aggregate them to create a very flexible and powerful application. It would be even more interesting to have each tool programmed in the language and framework that best fits it's purpose or best fits the skills of the programmers who are getting their hands dirty... but, then, we run into the risk of getting to something like Tex: a package that is again very heavy and hard to put together.

And there is one thing that both Damien Katz and the suckless guys agree upon: "[Go is the closest thing to a C replacement on the horizon, but it's not there yet. Ton of potential and nicer syntax.](https://twitter.com/damienkatz/status/289575389641179137)"