# CARTELS! — A Computational Classnotes Comic

A flippable, American-style comic book about cartels: six definitions and seventeen real cases from 1986–2026, narrated by **Investigator Lucval** and **Kirari-chan (キラリちゃん)**.

- **One file:** `index.html` contains everything: pages, characters, all 17 figures (embedded) and scripts. Only the comic fonts load from Google Fonts. Offline, the page falls back to system fonts and still works.
- **Built for phones:** the page fits any screen, in portrait or landscape. To turn pages, swipe left or right, tap the right or left half of the page, or use the BACK / NEXT buttons and the page list. Pinch to zoom in on small text; page turning pauses while you're zoomed.
- **Desktop:** use the ← and → keys or the space bar.
- **Links:** each page has its own address (`#p1`, `#p2` … `#p25`), so you can link straight to a page, e.g. `…/index.html#p6` for Case 3.

## What's in this folder

| File | Purpose |
|---|---|
| `index.html` | The whole comic |
| `README.md` | This guide |
| `LICENSE.md` | Licence (CC BY-NC-SA 4.0) |

---

## Option A: upload with the GitHub website (no software needed)

1. Sign in at <https://github.com> and click **+ → New repository**.
2. Name it, for example `cartels-comic`. Choose **Public** (needed for free GitHub Pages hosting) and click **Create repository**.
3. On the new repository page, click **uploading an existing file** (or **Add file → Upload files**).
4. Unzip `cartels-comic.zip` on your computer. Open the `cartels-comic` folder and drag **all three files** (`index.html`, `README.md`, `LICENSE.md`) into the browser window.
   *Drag the files, not the folder, so that `index.html` sits at the top level of the repository.*
5. Type a short message such as `Add Cartels comic` and click **Commit changes**.

## Option B: upload with git on the command line

```bash
# 1. Unzip and enter the folder
unzip cartels-comic.zip
cd cartels-comic

# 2. Turn it into a git repository and make the first commit
git init
git add .
git commit -m "Add Cartels comic"

# 3. Connect it to an EMPTY repository you created on GitHub
#    (replace YOUR-USERNAME and the repository name)
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/cartels-comic.git
git push -u origin main
```

If git asks for a password, use a **personal access token** (GitHub → Settings → Developer settings → Personal access tokens). Your account password won't work here. You can also sign in with GitHub Desktop or the `gh auth login` command.

**Updating later:** replace `index.html` with a new version, then run:

```bash
git add index.html
git commit -m "Update comic"
git push
```

---

## Publish it as a website (GitHub Pages)

1. In the repository, open **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose branch **main** and folder **/ (root)**, then click **Save**.
4. After a minute or two the comic is live at:
   `https://YOUR-USERNAME.github.io/cartels-comic/`

### Optional: serve it from your own domain

To put it under a subdomain such as `comic.justice.compclassnotes.com`:

1. In **Settings → Pages → Custom domain**, enter the domain and click **Save**. GitHub adds a `CNAME` file to the repository for you.
2. At your DNS provider, add a **CNAME** record pointing that subdomain to `YOUR-USERNAME.github.io`.
3. Once the certificate is issued, tick **Enforce HTTPS**.

If `justice.compclassnotes.com` is already hosted somewhere else, you can upload `index.html` to a folder there instead (e.g. `/cartels/`). It needs no server setup.

---

## Credits

**Production Team:** Principal Investigator: Lucval · Editors: Dara, Lucia · Software: FreeFormer · Agent: Kirari-chan (キラリちゃん)

Adapted from *Cartels: Definitions and Real Cases, 1986–2026* (13 November 2026). Character speech by the anonymous "suits" is dramatized; every fact is footnoted to its source inside the comic.

**© 2026 Computational Classnotes · CC BY-NC-SA 4.0** · <https://justice.compclassnotes.com/>
