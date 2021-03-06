+++
title = "Moving from Vim to Spacemacs"
author = ["Jean-Loup Adde"]
lastmod = 2020-04-19T13:47:23+01:00
tags = ["spacemacs", "vim"]
draft = false
+++

It's been five years I am now in the "Software Engineering" industry and I've been playing with few editors. I have to admit it became quite a meme around me as I love playing around with the different type there's out there. VS Code, Vim, Emacs, IntelliJ, PyCharm & others. Seriously, it's time consuming. As you might have guessed, this post will be about my transition from 4 years (yeah I was one year on PyCharm even though the technical beast sitting next to me was praising the benefits of Vim every single day) of using Vim intensively to use Spacemacs for literally everything.
I am sure you've seen few posts "_why I moved from X to Y and here's why you should do the same_". I don't agree with that. The good takes from posts like this are only if you experience the same issues with your current editor than the author. There's no "better" editor out there (sadly). They all come with trade offs so it's like any engineering solution you'll take. Just choose wisely. I'll spend a bit of time giving you the context then and hopefully you'll find this post helpful.

{{< figure src="/post_content/moving-from-vim-to-emacs/spacemacs_logo.png" >}}


## Some context {#some-context}

I moved from being a Web Developer to a Systems Engineer / Site Reliability Engineer / Platform Engineer (TL;DR; software engineering -> Infra / Cloud Architecture). During my year as a Web Developer, I used PyCharm as my main IDE. To be honest, it was a great experience. I loved live-debugging. As I was working on only one Django project all the time it was perfect. I learned a lot of Django by just digging into its mechanics and how it was dealing with the variables, views and all its goodness.
However, when I moved to a pluridisciplinary job, that's where I could feel this was not the right tool for everything. Even building python scripts. It was literally using an overpowered tool for a simple job. So I decided to move to Vim. I spent quite a lot of time to build a similar experience but with the tool that felt enough to have a confortable development experience.

Syntax highlighting, Syntax checkers, Linters and auto-completion when possible.


## Why? {#why}

If you move away from something, you better have a reason, right? Or I guess that would be called madness or boredom... My main problem was that my setup was really flaky and the time consumed to produce it was quite crazy. As well for a "simple editor", my vim was taking over 30/40 seconds to startup which can be quite irritating. So, I was still looking for a better alternative. I gave a shot to VS code, I just struggled as the navigation was not keyboard friendly. At the time, I was mainly in the terminal so having a dedicated app for the editor did not make sense **and** the editor is clearly made to be used with a mouse not keyboard first. So, I always ended up going back to vim. Until a colleague a year ago got a little bit pushy regarding emacs and spacemacs more particularly. I gave it a shot and after few times going back to vim, I finally moved over Spacemacs for good.

**Pros:**

1.  Spacemacs is a crowd configured "Emacs setup"
2.  Spacemacs is highly configurable
3.  Spacemacs can be used with Vim bindings :heart:
4.  Spacemacs bindings are mnemonic **and discoverable**
5.  Proper programming language to configure the editor (even if it's Lisp _sigh_)

**Cons:**

1.  Learn how Emacs works
2.  Learn Lisp :sweat_smile:
3.  Can get overwhelming with all the tools/packages Spacemacs provides


## How? {#how}

If you want to give it a try, it's fairly simple, install emacs on your machine and install the spacemacs config in \`~/.emacs.d\`.
You can then navigate through the shortcuts by just pressing "Space". You'll get a quick overview of shortcuts available: p for projects, w for window, b for buffer etc... And so on if you continue deep down. So you'll end up with smashing your space bar every time you want to do something with Spacemacs.
To be honest, I never thought I would memorise so easily all those shortcuts. The best one is space + space where you can search for functions like ctrl+P on VS Code. It's pretty neat.


## So... All good now? {#so-dot-dot-dot-all-good-now}

Well... I still spend an awful time configuring Spacemacs. First the learning curve was a bit stiff. Then learning all the packages. Then reading the packages and the layers (yeah I like to know how it works).

I'll never go back to Vim though and that's for sure. Now I discovered org-mode and I am using it quite intensively, I don't feel I can move to any editor. I'll write a post later on org-mode especially which I find the best way to take notes and keep your productivity to the roof.

There's still some flaky elements like lsp integration, auto-completion which I am not quite about about but I started living without. It's not like I am writing complicated software and if I have to dig inside the doc, it's probably a good thing to force me read a bit.

So, should you stick to your massive IDE or try a simple text editor? Well.. If you want the later with the functionality of the first, you're signing to a long journey into discovering the innards of your editor, being part of a community and starting contributing to it. If you simply want to gain in productivity with your editor, just learn the shortcuts. Glad mine is only usable with those :joy:.
