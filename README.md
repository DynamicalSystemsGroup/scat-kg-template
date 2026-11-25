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

It prints what it found, in plain words. Run it again after every change. Other commands (`scat status`, `scat index`, `scat stub`, `scat record-edge`, `scat set-status`) are in the guides.

Prefer working interactively? The same check runs in the Python REPL. Start it with `uv run python`, then type these two lines:

```
import scat_kg
scat_kg.check()
```

Each command has a twin in the REPL, such as `scat_kg.status()`.

## See the whole picture

`analysis.ipynb` shows the vault's views: each narrative's fingerprint, the edge tables, the layered view and traces. It writes nothing into your pages. Open it with `uv run jupyter lab analysis.ipynb` and choose **Run > Run All Cells**.

## 4. Open it in Obsidian

After cloning, open Obsidian (version 1.9 or later, which the index pages need), choose **Open folder as vault**, and pick the cloned folder (`my-vault`). Create pages with `scat stub`, which refuses a bad name and says why. The guides show how.

## What this is

A template for turning facilitated discussions into a knowledge graph. It is an [Obsidian](https://obsidian.md) vault kept in git. A **node** is one page, in one of four layers: **S**takeholder groups (a `group` page), **C**oncerns, **A**ffordances and **T**echnologies (SCAT). A **narrative** is one page too: an account with a link wherever it names a node, and a table headed `Edges told` with one row for each edge the account tells: its type (`holds`, `is addressed by` or `is provided by`), the node it comes from, the node it goes to, and a note. An edge is a row, never a page. The tool builds the knowledge graph from the pages on every call, and the small `scat` tools check them as you go.

Each type has an **index page**, a Base in `index/` that lists its pages and stays current by itself. Obsidian's table editor re-pads a table when you click into it. That is harmless: the tool reads the table whatever its spacing.

A remark between two entries of one type, such as two concerns that pull against each other, is a plain line in the body of one of them with a link to the other. The tool gives it no meaning.

The vault ships with a worked example: the elicitation of scat-kg itself, coded as two scenarios and two architectures. It is only there to show you the shape. Delete it or overwrite it with your own. Its groups are named by role, in the Chatham House style, so no individual is identifiable. Do the same in yours.

## Guides

The guides for planning, facilitating and coding are on the docs site: <https://dynamicalsystemsgroup.github.io/scat-kg-tools/>.
