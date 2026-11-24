# scat-kg-template

**Start here: step 1.** Type every command below in Terminal.

## 1. Create your repository (keep it private)

Your discussions are your data, so make your repository **private**. Pick one path.

**With the GitHub CLI.** You need `gh` and a one-time `gh auth login`. No `gh`? Use the website path below.

```
gh repo create my-vault --template DynamicalSystemsGroup/scat-kg-template --private --clone
cd my-vault
```

**On the GitHub website.** Open this repository, choose **Use this template**, then **Create a new repository**, set the visibility to **Private**, and create it. Then, using the address GitHub shows for your new repository:

```
git clone <the address of your new repository>
cd my-vault
```

## 2. Set up

You need a Mac with `git`. Install `uv` once (it fetches Python 3.12 itself):

```
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Open a new Terminal window, go to your folder (`cd my-vault`), and run the one setup command:

```
uv sync
```

## 3. Take your first step

Check the vault:

```
uv run scat check
```

It prints what it found, in plain words. Run it again after every change. Other commands (`scat status`, `scat index`, `scat stub`) are in the guides.

Prefer working interactively? The same check runs in the Python REPL. Start it with `uv run python`, then type these two lines:

```
import scat_kg
scat_kg.check()
```

Each command has a twin in the REPL, such as `scat_kg.status()`.

## 4. Open it in Obsidian

After cloning, open Obsidian, choose **Open folder as vault**, and pick the cloned folder (`my-vault`). Create pages with `scat stub`, which refuses a bad name and says why. The guides show how.

## What this is

A template for turning facilitated discussions into a knowledge graph. It is an [Obsidian](https://obsidian.md) vault kept in git. Each page records one thing the group said, in four kinds: **S**takeholders, **C**oncerns, **A**ffordances and **T**echnologies (SCAT). Small `scat` tools check the pages as you go.

The vault ships with a worked example: the elicitation of scat-kg itself. It is only there to show you the shape. Delete it or overwrite it with your own. Its stakeholders are groups named by role, in the Chatham House style, so no individual is identifiable. Do the same in yours.

## Guides

The guides for planning, facilitating and coding are on the docs site: <https://dynamicalsystemsgroup.github.io/scat-kg-tools/>.
