---
sidebar_position: 1
---

# Manage Docs Versions

Docusaurus can manage multiple versions of your docs.

**Versioning** in Docusaurus allows us to maintain multiple versions of our documentation. This is especially useful for projects that undergo frequent updates, ensuring that users can access documentation relevant to their specific software version.

For example, if you release a new version of your product (e.g., v2.0), older users can still refer to documentation for v1.0.

## How Versioning Works

When you enable versioning, Docusaurus **snapshots** your current documentation and moves it into a versioned folder. This helps maintain historical versions while continuing to update the latest documentation.

## Steps to Enable Versioning

### Initialize Versioning

Run the following command in your terminal to create the first versioned documentation:

```bash
npm run docusaurus docs:version 1.0
```

This will:

- Create a `versioned_docs/` directory containing the current docs as `version-1.0`.
- Create or Update `versions.json` with the version history.
- Retain the `latest (unversioned)` docs as the default.

Your docs now have 2 versions:

- `1.0` at `http://localhost:3000/docs/` for the version 1.0 docs
- `current` at `http://localhost:3000/docs/next/` for the **upcoming, unreleased docs**

### Managing a Version

- The latest documentation remains in `/docs/` (for ongoing updates).
- Older versions are stored in `/versioned_docs/`.
- The `versions.json` file keeps track of available versions.

Example of versions.json:

```bash
[
  "1.0"
]
```

### Add a Version Dropdown

To navigate seamlessly across versions, add a version dropdown.

Modify the `docusaurus.config.js` file:

```js title="docusaurus.config.js"
export default {
  themeConfig: {
    navbar: {
      items: [
        // highlight-start
        {
          type: "docsVersionDropdown",
        },
        // highlight-end
      ],
    },
  },
};
```

The docs version dropdown appears in your navbar:

![Docs Version Dropdown](./img/docsVersionDropdown.png)

### Update an existing version

It is possible to edit versioned docs in their respective folder:

- To edit the latest documentation, update files inside /docs/.
  - `docs/hello.md` updates `http://localhost:3000/docs/next/hello`
- To update an older version, modify files inside /versioned_docs/version-1.0/.
  - `versioned_docs/version-1.0/hello.md` updates `http://localhost:3000/docs/hello`

### Deleting Old Versions

To remove a version, manually delete its folder from `versioned_docs/` and update `versions.json` accordingly.
