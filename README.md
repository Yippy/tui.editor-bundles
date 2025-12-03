# tui.editor-bundles
tui.editor-bundles for TeebbTuiEditorBundle public assets.

Using Node Package Manager (npm) to retrieve the latest files.

To be able to compile the prosemirror you need to create a bundle. You can do this with babelify/browserify.

```
npm install --save-dev babelify @babel/core
```

The package.json will run a script when using this command to output the prosemirror-bundle needed to TUI Editor.

```
npm run build
```

> [!NOTE]
> browserify index.js --outfile prosemirror-bundle.js"
