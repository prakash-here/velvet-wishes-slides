# Velvet Wishes — cloud content

Public on purpose: Instagram fetches carousel slides from raw URLs, and other
tools read product images from here. Everything that needs a public address
lives in a folder named for what it is, never loose at the root.

    carousels/<slug>/   slide sets pushed for publishing (JPEGs from
                        workflows/05-carousel-maker/out/<slug>/upload)
    reels/<slug>/       reel files or poster frames that need a public URL
    catalog/<product>/  product images used away from the storefront
    misc/<topic>/       anything else, named by its purpose

Upload with:

    python workflows/05-carousel-maker/push_slides.py --folder <out folder>

It writes `public-urls.txt` beside the slides for `ig_publish.py --urls`.
Re-running over the same slug overwrites the same filenames, so links stay
stable. Nothing here is private — treat every file as published.
