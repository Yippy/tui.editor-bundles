# tui.editor-bundles
tui.editor-bundles for TeebbTuiEditorBundle public assets.

Using Node Package Manager (npm) to retrieve the latest files.

# Maintaining this Bundle
This repository has already been compiled, but if you wish to update and compile your own bundles, the package.json can run a script using these command to output specific bundle that is needed.

Firstly to be able to compile you need browserify.

`npm install --save-dev babelify`

npm install --no-package-lock --no-save pako`
TUI Editor
`npm run build_editor`
> [!NOTE]
> This will run this command:
> `browserify ./modules/export-toast-ui-editor.js --s Editor --outfile toast-ui-editor-bundle.js`

Plugin to render chart
`npm run build_chart`
> [!NOTE]
> This will run this command:
> `browserify ./modules/export-toast-ui-editor-plugin-chart.js --s chart --outfile toast-ui-chart-bundle.js`

Plugin to highlight code syntax
`npm run build_code_syntax_highlight`
> [!NOTE]
> This will run this command:
> `browserify ./modules/export-toast-ui-editor-plugin-code-syntax-highlight.js --s codeSyntaxHighlight --outfile toast-ui-code-syntax-highlight-bundle.js`

Plugin to color editing text
`npm run build_color_syntax`
> [!NOTE]
> This will run this command:
> `browserify ./modules/export-toast-ui-editor-plugin-color-syntax.js --s codeColorSyntax --outfile toast-ui-color-syntax-bundle.js`

Plugin to merge table columns
`npm run build_table_merged_cell`
> [!NOTE]
> This will run this command:
> `browserify ./modules/export-toast-ui-editor-plugin-table-merged-cell.js --s codeColorSyntax --outfile toast-ui-table-merged-cell-bundle.js`

Plugin to render UML