# TestTokensPlugin
Test repository for Figma Tokens Plugin

Single-file theme:
Run token-transformer: npx token-transformer tokens.json tokens/input.json
Build with style-dictionary: npx style-dictionary build --config config.json

Multi-file themes:
- Transform Figma Tokens JSON to something Style Dictionary can read
    run: npx token-transformer tokens.json tokens/global.json global

- Create a light theme, exclude the global tokens
    run: npx token-transformer tokens.json tokens/light.json global,light,theme global
- Create a dark theme, exclude the global tokens
    run: npx token-transformer tokens.json tokens/dark.json global,dark,theme global
- Convert tokens according to Style Dictionary config
    run: node build.js
