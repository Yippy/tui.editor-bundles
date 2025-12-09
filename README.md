# tui.editor-bundles
tui.editor-bundles for TeebbTuiEditorBundle public assets.

Using Node Package Manager (npm) to retrieve the latest files.

# Maintaining this Bundle
This repository has already been compiled, but if you wish to update and compile your own bundles, the package.json can run a script using these command to output specific bundle that is needed.

Firstly to be able to compile you need browserify.

`npm install --save-dev babelify`

`npm install --no-package-lock --no-save pako`

TUI Editor - These build command were tested on Windows OS
`npm run build_editor`
> [!NOTE]
> This will run this command:
> `browserify ./modules/export-toast-ui-editor.js --s Editor --outfile ./public/js/toast-ui-editor-bundle.js && cp 'node_modules/@toast-ui/editor/dist/toastui-editor.css' ./public/css && cp 'node_modules/@toast-ui/editor/dist/theme/toastui-editor-dark.css' ./public/css && cp 'node_modules/jquery/dist/jquery.min.js' ./public/js`

TUI Viewer
`npm run build_editor`
> [!NOTE]
> This will run this command:
> `browserify ./modules/export-toast-ui-viewer.js --s Viewer --outfile ./public/js/toast-ui-viewer-bundle.js && cp 'node_modules/@toast-ui/editor/dist/toastui-editor-viewer.css' ./public/css`

Plugin to render chart
`npm run build_chart`
> [!NOTE]
> This will run this command:
> `browserify ./modules/export-toast-ui-editor-plugin-chart.js --s chart --outfile ./public/js/toast-ui-chart-bundle.js && cp 'node_modules/@toast-ui/chart/dist/toastui-chart.min.css' ./public/css`

Plugin to highlight code syntax
`npm run build_code_syntax_highlight`
> [!NOTE]
> This will run this command:
> `browserify ./modules/export-toast-ui-editor-plugin-code-syntax-highlight.js --s codeSyntaxHighlight --outfile ./public/js/toast-ui-code-syntax-highlight-bundle.js && cp 'node_modules/@toast-ui/editor-plugin-code-syntax-highlight/dist/toastui-editor-plugin-code-syntax-highlight.css' ./public/css`

Plugin to color editing text
`npm run build_color_syntax`
> [!NOTE]
> This will run this command:
> `browserify ./modules/export-toast-ui-editor-plugin-color-syntax.js --s colorSyntax --outfile ./public/js/toast-ui-color-syntax-bundle.js && cp 'node_modules/@toast-ui/editor-plugin-color-syntax/dist/toastui-editor-plugin-color-syntax.css' ./public/css && cp 'node_modules/tui-color-picker/dist/tui-color-picker.css' ./public/css`

Plugin to merge table columns
`npm run build_table_merged_cell`
> [!NOTE]
> This will run this command:
> `browserify ./modules/export-toast-ui-editor-plugin-table-merged-cell.js --s tableMergedCell --outfile ./public/js/toast-ui-table-merged-cell-bundle.js && cp 'node_modules/@toast-ui/editor-plugin-table-merged-cell/dist/toastui-editor-plugin-table-merged-cell.css' ./public/css`

Plugin to render UML
`npm run build_table_merged_cell`

Oddly the UML Plugin requires packages that was location dependant, which has caused this lengthly command for copying all the dependencies in the correct location for UML Plugin to compile.

> [!NOTE]
> This will run this command:
> `(if not exist .\\node_modules\\plantuml-encoder\\dist\\zlib mkdir .\\node_modules\\plantuml-encoder\\dist\\zlib) && cp 'node_modules/pako/lib/zlib/trees.js' node_modules/plantuml-encoder/dist/zlib/ && cp 'node_modules/pako/lib/zlib/inftrees.js' node_modules/plantuml-encoder/dist/zlib/ && cp 'node_modules/pako/lib/zlib/inffast.js' node_modules/plantuml-encoder/dist/zlib/ && cp 'node_modules/pako/lib/zlib/crc32.js' node_modules/plantuml-encoder/dist/zlib/ && cp 'node_modules/pako/lib/zlib/adler32.js' node_modules/plantuml-encoder/dist/zlib/ && cp 'node_modules/pako/lib/zlib/deflate.js' node_modules/plantuml-encoder/dist/zlib/ && cp 'node_modules/pako/lib/zlib/gzheader.js' node_modules/plantuml-encoder/dist/zlib/ && cp 'node_modules/pako/lib/zlib/zstream.js' node_modules/plantuml-encoder/dist/zlib/ && cp 'node_modules/pako/lib/zlib/messages.js' node_modules/plantuml-encoder/dist/zlib/ && cp 'node_modules/pako/lib/zlib/constants.js' node_modules/plantuml-encoder/dist/zlib/ && cp 'node_modules/pako/lib/zlib/inflate.js' node_modules/plantuml-encoder/dist/zlib/ && cp 'node_modules/pako/lib/deflate.js' node_modules/plantuml-encoder/dist/ && cp 'node_modules/pako/lib/zlib/adler32.js' node_modules/plantuml-encoder/dist/ && cp 'node_modules/pako/lib/zlib/crc32.js' node_modules/plantuml-encoder/dist/ && cp 'node_modules/pako/lib/zlib/messages.js' node_modules/plantuml-encoder/dist/ && cp 'node_modules/pako/lib/zlib/inftrees.js' node_modules/plantuml-encoder/dist/ && cp 'node_modules/pako/lib/zlib/inffast.js' node_modules/plantuml-encoder/dist/ && cp 'node_modules/pako/lib/zlib/inflate.js' node_modules/plantuml-encoder/dist/ && cp 'node_modules/pako/lib/inflate.js' node_modules/plantuml-encoder/dist/ && cp 'node_modules/pako/lib/zlib/trees.js' node_modules/plantuml-encoder/dist/ && (if not exist .\\node_modules\\plantuml-encoder\\utils mkdir .\\node_modules\\plantuml-encoder\\utils) && (if not exist .\\node_modules\\plantuml-encoder\\dist\\utils mkdir .\\node_modules\\plantuml-encoder\\dist\\utils) && cp 'node_modules/pako/lib/utils/common.js' node_modules/plantuml-encoder/utils/common.js && cp 'node_modules/pako/lib/utils/common.js' node_modules/plantuml-encoder/dist/common.js && cp 'node_modules/pako/lib/utils/common.js' node_modules/plantuml-encoder/dist/utils/common.js && cp 'node_modules/pako/lib/utils/strings.js' node_modules/plantuml-encoder/dist/utils/strings.js && cp 'node_modules/plantuml-encoder/lib/decode64.js' node_modules/plantuml-encoder/dist/ && cp 'node_modules/plantuml-encoder/lib/encode64.js' node_modules/plantuml-encoder/dist/ && browserify ./modules/export-toast-ui-editor-plugin-uml.js --s uml --outfile ./public/js/toast-ui-uml-bundle.js`