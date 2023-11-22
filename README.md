# digital-content-initiative

**Initiative to preserve my digital content and reclaim my digital identity.**

This document outlines an initiative to take back a sense of ownership for the things I create and post to the internet. It provides methods for consolidating my writing files under one, open format roof. While the focus of this initiative is currently limited to my writing files, my hope is to expand the scope over time. 

Consider this document my attempt at learning in public. You are reading a first draft, complete with typos, clumsy prose, and unsourced jabber. It will improve over time, but I think there's some decent stuff in here already. 

The methods outlined are also a work in progress, and require iterative improvements. I'll continue to update this document as I better understand my writing workflow and efficiency needs. 

## Introduction

It started in the summer— this nagging sense that what I create doesn't belong to me. My Tiktoks, Tweets, Medium posts, Substack newsletters, Instagram stories, etcetera— those are all *my* creations. I was in the room when I made'em. So why does it all feel inaccessible?

After some reflection, I learned something about my creative approach. I wasn't posting the things I made, I was making things to post. 

I wrote *in* Medium. I recorded *in* TikTok. Not because it necessarily easier to create in a clumsy video editor. I did it out of habit. I did it because that's what I've been trained me to do. In-app creation became my creative workflow. As a result, I accepted a sort of second-class ownership for my creations. 

That framing is not accidental. Social media platforms want us creating content specifically for them. They want our ownership to feel estranged. 

The feeling was inescapable. Even while writing in a simple word processor I paid monthly to use. *Why couldn't I see my files outside the context of the app I made them in?*

From an unpublished rant:

> For each new sentence I write in Ulysses, I dig myself deeper into a hole I pay monthly to occupy. Each additional draft, is that much more effort to climb out if I wanted something new. And recently, I've had the itch climb out like an injured Batman in *The Dark Knight Rises*. Because, I'm starting to question the wisdom of paying five bucks in perpetuity for a glorified text file generator. One that won't save my writings to a local folder by default. 

Ok. That was a little melodramatic. Perhaps I was also working through some misplaced frustration. Ulysses is hardly the biggest culprit. Nonetheless, I moved back to iA Writer. And now, I'm on a mission. 

This initiative is my first pass at reclaiming ownership over the digital stuff I make. Through the fall. I've laid the foundation for an independent presence on the web. I created a custom site on a custom domain where I can publish my writings *first*. 

To my surprise, I'm not the only one out there who felt trapped in digital silos. Some would label the space I've made as part of the small web, or the indie web. 

Whatever you call it, I'm in. 


## Objectives

My primary objectives are to convert all writing files into archival formats (txt, md), and consolidate the collection into single iCloud folder (iA Writer app folder). I then want to design a process to maintain my collection using the principles outlined in this document. I hope to preserve my collection of personal and professional writing that outlives me and Microsoft Word. 

### Single-folder file system

Eliminating sub-folders as a method for file organization requires strong sort and filter capabilities (so I can find my files). I must standardize my files' metadata using a well-defined keys and values (see front matter). This standardization requires a strong understanding of my writing workflow and other patterns. 

### Normalized file formats

I want everything in text and markdown file formats— articles, posts, guides, presentations, speeches, diary entries, documentation, stories, poems, and grocery lists. 

Okay, maybe not grocery lists. 

### Benefits 


1. Strong sense of ownership for the things I write. 
2. Better preservation of my writing collection. Text files will outlive proprietary file formats, and preserve text in its natural state. 
3. Improved portability in and out of various platforms— blogs, presentation software, etc. My writing no longer feels "trapped" in Word, PowerPoint, or Ulysses. 
4. Improved ability to repurpose my guides, presentations, and other standardized copy. My bio preserved in a markdown file can export into virtually any format— HTML, Rich Text, plain text, PDF— then reused for websites, social media profiles, guest speaker panels, etc. 

## Challenges
Identified challenges to meeting my goals. This list is unfinished and will likely grow. 

### Digital sprawl
My files are currently scattered across iCloud Drive, local directories, and multiple platform silos on the web. Remembering a file's location, or even its existence, is a challenge. 

### Unchecked file formatting 
My writing collection lacks a common file format. Since I have no deliberate methods for maintaining a "master file," some of my writings are "trapped" in closed file formats like `.pages`, `.ppt`, `.pdf`, and other internet silos. I think I even have something in Sharepoint from a decade ago. 

### Curating the right technology 

(Work in progress)

### I like shiny things
Perhaps the largest contributor to my problem is me. I love a good writing app. Give me a polished UI and a few novel features, and you can have all my data. I don't have a plan to combat this behavior just yet, but I'm thinking about it. 
 

## Choosing software with shared values 

To meet my goals, I'll need software willing to keep my files accessible in open formats. This realization came while testing a novel presentation app called iA Writer. 

From my post [On iA Presenter and my mission to preserve my digital assets](https://fromjason.xyz/p/freelance/on-ia-presenter-and-my-mission-to-preserve-my-digital-assets/): 

> The tools we use to create should bend to our creations, not the other way around. Our creations (writing, photos, graphics, code, etc.) should exist independently, free to move around, reshape, and repurpose. If an app can't respect that, I don't want it.

### iA Writer
iA Writer is the hub for writing collection. It's my primary word processing tool and where I store my master files. 

- Saves files in `.txt` in `.md` formats 
- Files are visible in an iCloud app folder by default. 
- Rich exporting features: HTML, Rich Text, plain text, MS Word and more. 
- Supports open source standards like micropub. 
- Offers non-subscription purchase option. 

### iA Presenter
While a version 1 app, iA Presenter is my primary presentation tool. I'm working on converting my presentation collection to Markdown format for easy presentation creation. 

- Saves files in `.txt` in `.md` formats 
- Files are visible in a folder of my choosing by default. 
- Rich exporting features: HTML, Rich Text, MS PowerPoint (beta) and more. 
- Offers non-subscription purchase option. 

### Eleventy (11ty) 
Eleventy is wonderful a static site generator that I use for my blog, From Jason. 11ty allows me to design a site structure I want and use a wide variety of file formats. 

- Open source.
- Uses established technology like JavaScript. 
- Processes posts in markdown or plain text.
- Easy to port my writing files elsewhere if needed. 
- Generous licensing and free to use.
- Large community of supporters and contributors. 

### Micro.blog (experimental)

(Work in progress)

### Open standards built on Indie Web tenets 

(Work in progress)

## Methods

### Front matter
Each file has a set of YAML-compliant keys and values that act as a type of metadata called front matter. My files' front matter  helps me to sort, filter, categorize, and process to the web. Furthermore, front matter helps me identify which of my writings I've published, abandoned (more likely forgotten), or require further editing regardless of publish status. 

#### Front matter keys and values
All front matter keys currently in use, with descriptions and value options. 

| key | value | options | definition | dependencies |
|--|--|----|-------------------|--|
| `draft` | boolean | `true`, `false` | Identifies a file as incomplete, unpublished, or both. | Smart Folder, 11ty (false value) |
| `expat` | boolean | `true`, `false` | files once published on other platforms that I've added to my collection. Expat files with `draft` set to `true` have yet to be republished to my blog. | Smart Folder |
| `archive` | boolean | `true`, `false` | unpublished, abandoned, and/or old drafts I have no intentions to use. | Smart Folder |
| `type` | string | `siteCopy`, `presentation`, `readMe`, `prompt`, `note`, `essay`, `series`, `page` | Defines the type of content within the file. value options are loosely defined at the moment. | Smart Folder, 11ty |
| `site` | string | `fromJason` | Identifies where the file was published. | Smart Folder |
| `phase` |  | `sorting`, `deadEnd` | Identifies how "polished" the concept is. The phase value options are also loosely defined at the moment. I need to flush out a better system.  | Smart Folder, From Jason |
| `sub` | string | `notebook`, `freelance`, `stories`, `travel` | Assigns a post to a blog section. | Smart Folder, From Jason |
| `title` | string |  | Title of file. Will slugify for url | 11ty, Smart Folder (1 exception) |
| `description` | string |  | Short summary of file | 11ty, Open Graph |
| `date` | yyyy-mm-dd |  | Published date of file. | 11ty |
| `audience` | string |  | Assumed audience for post. | From Jason |
| `graphic` | file name ext | '23.png' | The primary graphic for From Jason posts | From Jason |
| `graphicAlt` | string | 'illustration of...' | Alt text for graphic | 11ty |
| `tags` | array | ['tag 1', 'tag 2'] | Tags for posts | 11ty |

#### Front matter templates
Front matter templates are defined in the `title` key with a `frontMatter` value. I manually copy the a template's contents and paste into my files as needed. Since there is currently no "source of truth" for my front matter, I try to keep the templates DRY. 

- Standard posts: [[frontMatter]]
- Site copy: [[frontMatter siteCopy]]
- Dead ends: [[frontMatter deadEnd]]

### iA Smart Folders
Files are filtered into ia Writer's "smart folders" using front matter keys and values, or file extension. 

#### Filter by front matter

Primary front matter filters:
- sub
- type
- phase
- site
- archive
- draft
- expat

#### Filter by `title` for templates

The title key is typically reserved for the H1 post titles and/or to slugify a post url. Reusable front matter templates are an exception. Rather than creating a special "template" key that I'd have to delete each time I paste the template into my post, I assign a `frontMatter` value to the `title` key. I still need to replace the value with the post's title, but the chances of forgetting are less this way. 

#### Filter by `.md` and `.txt` file extension

Assigning meaning to file extensions help me better filter files in iA Writer smart folders:
- Markdown files (`.md`) are for publishing (i.e. to my blog or presentation software like iA Presenter). 
- Text files (`.txt`) are private documentation, templates, etc. 

## Unfinished documentation 

#### Attempt to define `phase` values
Identifies how "polished" the concept is. The phase value options are also loosely defined at the moment. I need to flush out a better system. 

1. Sorting (and assembling)
2. Matching (and fitting)
3. Assembling (with interlocking)
4. Deconstructing 

1. Aligning: When putting a puzzle together, you align the edges and shapes of the pieces to ensure they fit together correctly.
2. Matching: This involves finding and matching similar patterns, colors, or shapes on adjacent puzzle pieces.
3. Fitting: As you work on the puzzle, you aim to find the correct placement and fit for each piece within the larger picture.
4. Assembling: This refers to the act of putting the puzzle pieces together to form the complete picture.

