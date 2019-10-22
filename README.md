# Why isn't `.gitignore_global` working for me…

While working on [a repo to house some javascript practice](https://github.com/dotsara/gui-practice), I started seeing `.DS_Store` showing up in `git status`. 

😐

Except, I have a `.gitignore_global` file, so what gives?

The usual searching and StackOverflowing got me loooots of cranky "this is a duplicate of…" posts, but while rubber ducking for myself, I decided to start from "the beginning". Check the steps for adding a `.gitignore_global` in the first place and see if I need to…&nbsp;do it again?

In the middle of it, I wondered if the upgrade to macOS Catalina and the new default shell of `zsh` instead of `bash` might have to do with it? Is it possible "just" making that change in System Preferences somehow skips? ignores (heh)? that file? 

So, I made this test repo, added files in the GitHub web UI, then cloned it down to my machine. Added a couple of files locally (in Finder) and checked `git status`. 💥 `.DS_Store` appears. 

Then I deleted the folder in Finder, deleted my `.gitignore_global` file (but not before copying out the contents), restarted the machine, and re-created `.gitignore_global`. 

After adding files locally (in the main repo and in a directory), I checked `git status` and woohoo! No more `.DS_Store` files. 

`:carlton_dance:`

I did consider that maybe I "just" needed to restart my machine, post-`zsh` switch, but a. I _think_ I have restarted since then and b. I can't test, now. (Or anyway, to retest it now is way more effort than it's worth for me just now).

22-Oct-2019