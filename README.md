### Hi there 👋
- ⚙ Atualmente eu trabalho como tecnico em hardwere
- 🌱 Estou aprendendo programação web
- 💬 Tenho o sonho de trabalhar com programação e vou fazer acontecer
- ⚡ Sou programador junior em linguagem c

  "preview-theme": "node scripts/preview-theme",
    "close-stale-theme-prs": "node scripts/close-stale-theme-prs",
    "generate-langs-json": "node scripts/generate-langs-json",
    "format": "./node_modules/.bin/prettier --write .",
    "format:check": "./node_modules/.bin/prettier --check ."
    "format": "prettier --write .",
    "format:check": "prettier --check .",
    "prepare": "husky install"
  },
  "author": "Anurag Hazra",
  "license": "MIT",
@@ -27,10 +28,11 @@
    "axios-mock-adapter": "^1.18.1",
    "color-contrast-checker": "^2.1.0",
    "hjson": "^3.2.2",
    "husky": "^4.2.5",
    "husky": "^8.0.0",
    "jest": "^29.0.3",
    "jest-environment-jsdom": "^29.0.3",
    "js-yaml": "^4.1.0",
    "lint-staged": "^13.0.3",
    "lodash.snakecase": "^4.1.1",
    "parse-diff": "^0.7.0",
    "prettier": "^2.1.2"
@@ -43,9 +45,7 @@
    "upgrade": "^1.1.0",
    "word-wrap": "^1.2.3"
  },
  "husky": {
    "hooks": {
      "pre-commit": "npm test"
    }
  "lint-staged": {
    "*.{js,css,md}": "prettier --write"
  }
}
