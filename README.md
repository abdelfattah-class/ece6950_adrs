Forked from computer-networks/15-744-sp20 (credit goes to Prof. Justine Sherry)

# Adding your class project page

Every project gets a tile on the **Class Projects** page and its own page with
your video, final report, and a write-up. You only need to add one Markdown
file and a folder of assets — no HTML required.

## 1. Pick a short name for your team

Use lowercase letters, numbers, and dashes only, e.g. `kernel-tuning-agents`.
Below, this is called `<team-name>`. Your page will live at
`project-<team-name>.html`.

## 2. Add your files

```
_projects/<team-name>.md                     <- your project page (copy the sample)
assets/projects/<team-name>/thumbnail.png    <- tile image, 16:9 (e.g. 1280x720)
assets/projects/<team-name>/report.pdf       <- your final report
assets/projects/<team-name>/...              <- any figures you use on your page
```

Start by copying the sample:

```bash
cp _projects/sample-project.md _projects/<team-name>.md
mkdir -p assets/projects/<team-name>
```

## 3. Fill in the top of your file

The block between the two `---` lines controls the tile and page header:

| Field       | What to put there |
|-------------|-------------------|
| `title`     | Your project title (keep the quotes). |
| `team`      | Team members, e.g. `["Ada Lovelace", "Alan Turing"]`. |
| `tagline`   | One sentence shown on the tile and under the title. |
| `thumbnail` | `assets/projects/<team-name>/thumbnail.png` |
| `youtube_id`| The ID from your YouTube link: for `https://www.youtube.com/watch?v=dQw4w9WgXcQ` use `dQw4w9WgXcQ`. For `youtu.be/XYZ` links, use `XYZ`. Make the video *Public* or *Unlisted*. |
| `report`    | `assets/projects/<team-name>/report.pdf` (or a full URL, e.g. arXiv). |
| `code`      | Optional link to your repository. Delete the line if you don't have one. |

**Delete the `sample: true` line** in your copy.

Any field you don't need can be deleted; the page simply leaves that part out.

## 4. Write your summary

Everything below the second `---` is regular Markdown: headings (`##`),
lists, **bold**, tables, links, and images. For images, use paths like
`![My figure](assets/projects/<team-name>/fig1.png)` — no leading slash.

## 5. Submit

Open a pull request with your two additions (`_projects/<team-name>.md` and
`assets/projects/<team-name>/`). Please don't edit other teams' files or the
layouts.

### Preview locally (optional)

```bash
gem install jekyll
jekyll serve
# then open http://localhost:4000/projects.html
```
