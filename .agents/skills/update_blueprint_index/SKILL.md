---
name: update_blueprint_index
description: A skill that is invoked when asked to update the blueprint index.
---

# Update Blueprint Index

When you are asked to update the blueprint index, perform the following steps carefully:

1. Locate the directory `c:/ws/orchestra-local/blueprints` and iterate through all the markdown (`.md`) files it contains.
2. For each file, inspect its YAML frontmatter to extract the `title` and `description` properties. Also, check if there is a `private` property.
3. Skip any file that contains `private: true` in its frontmatter. 
4. For the remaining non-private files, construct an entry using the following exact format:
   `  - **{title}** - {description} (*./blueprints/{filename}*)`
5. Compile these entries together into a single list.
6. Overwrite the file `c:/ws/orchestra-local/blueprint-index.md` with:
   - A single top-level header: `# Blueprint repository index  `
   - Two empty lines.
   - The compiled list of entries.

**Example output format for blueprint-index.md**:
# Blueprint repository index  


  - **Writing a blog post** - Allows the user to write a professional blog post (*./blueprints/blog.md*)
  - **Writing a Post on X** - Allows the user to draft a Post on X (formerly called "Tweet on Twitter", now sometimes called "X on X") (*./blueprints/tweet.md*)
