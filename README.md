# scat-kg-template

A template for turning facilitated discussions into a knowledge graph. It is an [Obsidian](https://obsidian.md) vault kept in git. Each page records one thing the group said, in four kinds: **S**takeholders, **C**oncerns, **A**ffordances and **T**echnologies (SCAT). Small `scat` tools check the pages as you go.

The vault ships with a worked example: the elicitation of scat-kg itself. It is only there to show you the shape. Delete it or overwrite it with your own. The example's stakeholders are groups named by role, in the Chatham House style, so no individual is identifiable. Do the same in yours.

## 1. Create your repository (keep it private)

Your discussions are your data, so make your repository **private**. Pick one path.

**Command line** (needs the [GitHub CLI](https://cli.github.com/), `gh`), with Private already chosen:

```
gh repo create my-vault --template DynamicalSystemsGroup/scat-kg-template --private --clone
```

**GitHub website:** open this repository, choose **Use this template**, then **Create a new repository**, set the visibility to **Private**, and create it. Then clone it:

```
git clone <the address of your new repository>
```

## 2. Set up

You need a Mac, `git`, and `uv`. Install `uv` with the command on <https://docs.astral.sh/uv/> (the curl installer). `uv` fetches Python 3.12 itself.

Then, inside your cloned folder, run the one setup command:

```
uv sync
```

## 3. Take your first step

Check the vault. In the Python REPL:

```
uv run python
>>> import scat_kg
>>> scat_kg.check()
```

The same check on the command line:

```
uv run scat check
```

It prints what it found, in plain words. Run it again after every change. Other commands (`scat status`, `scat index`, `scat stub`, and more) are in the guides, each with a twin in the REPL such as `scat_kg.status()`.

## 4. Open it in Obsidian

In Obsidian, choose **Open folder as vault** and pick your cloned folder. The page templates for the four kinds of record are already set up.

## Guides

The guides for planning, facilitating and coding are on the docs site: <https://dynamicalsystemsgroup.github.io/scat-kg-tools/> (planned address; not live yet).
