---
"@open-slide/core": minor
---

Add multi-level folder nesting to the slide organizer.

- Folders can now have a `parentId`, so they nest arbitrarily deep. The sidebar renders the folder tree with expand/collapse, and folder counts are recursive (a folder counts its own slides plus all descendants').
- Selecting a parent folder lists its own decks first, then the decks of each descendant subfolder grouped under a labelled section.
- New built-in **"All slides"** view that lists every slide regardless of folder, alongside the existing Draft (unassigned) bucket.
- The folder "Move under" menu renders nested submenus, and the slide "Move to folder" dialog renders a collapsible tree, so relocating items stays manageable as the folder structure grows.
- Folder create/patch accept `parentId` (validated against cycles and self-parenting); deleting a folder re-parents its children onto the deleted folder's parent.
- The `create-slide` skill documents the folder model so authoring agents place decks in the right (leaf) folder.
