# Custom Markdown Syntax Highlighter

Part of my writing-workflow is a post [processing script](https://github.com/saschakiefer/workflow-support), that turns a custom inline footnote string with the format `{{fn: }}`into a numbered footnote list, that is also compatible with git.

This plugin enables syntax highlighter for this string. With the following settings, the inline footnote can be colored a bit less disruptive, so the text is more readable:
```json
"editor.tokenColorCustomizations": {
    "textMateRules": [{
        "scope": "string.quoted.other.footnote",
        "settings": {
            "foreground": "#4b4b4b",
            "fontStyle": "italic"
        }
    }]
}
```

## Helpful Resources

Developing such a plugin is not very well documented. The following resources were quite helpful:

* [Syntax Highlight Guide](https://code.visualstudio.com/api/language-extensions/syntax-highlight-guide#scope-inspector)
* [TextMate Language Grammars](https://macromates.com/manual/en/language_grammars)
* [TextMate Regular Expressions](https://macromates.com/manual/en/regular_expressions)
* [Injecting Front Matter Syntax Highlighting in Markdown Files](https://www.marcobeltempo.com/open-source/inject-frontmatter-syntax-markdown/)
* [VSCode Markdown Fenced Code Block Grammar Injection Example](https://github.com/mjbvz/vscode-fenced-code-block-grammar-injection-example)
