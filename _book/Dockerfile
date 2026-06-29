# Runs the GitBook site via HonKit — the maintained, drop-in successor to the
# (now-defunct) legacy `gitbook-cli`. It reads the same book.json / SUMMARY.md /
# Markdown content, so no source changes are required.
FROM node:20-slim

WORKDIR /book

# Install the GitBook-compatible engine. Done before copying the content so the
# dependency layer is cached. Installed locally to match the compose anonymous
# volume on /book/node_modules.
COPY package.json book.json ./
RUN npm install honkit@6 && npm cache clean --force

# Copy the book sources (content/, SUMMARY.md, README.md, ...).
COPY . .

# Web server (4000) + LiveReload (35729). HonKit serves on 0.0.0.0 by default.
EXPOSE 4000 35729

CMD ["npx", "honkit", "serve", ".", "--port", "4000"]
