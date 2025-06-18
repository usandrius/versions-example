# Nuxt Minimal Starter

Look at the [Nuxt documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Setup

Make sure to install dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.

---

## Разработка и релизы

В этом проекте используется стандарт [Conventional Commits](https://www.conventionalcommits.org/ru/v1.0.0/) для сообщений коммитов. Это позволяет автоматизировать управление версиями и генерацию списка изменений (CHANGELOG).

### Создание коммитов

Чтобы гарантировать правильный формат сообщений, используйте один из следующих способов:

1.  **Через командную строку (рекомендуется для универсальности):**
    ```bash
    npm run commit
    ```
    Эта команда запустит интерактивный помощник `commitizen`, который задаст вам несколько вопросов и сформирует правильное сообщение коммита.

2.  **Через интерфейс VS Code/Cursor:**
    Установите расширение [Conventional Commits](https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits). После установки в панели "Source Control" появится иконка круга. Нажмите на нее, чтобы запустить интерактивный конструктор коммитов.

> **Важно:** Если вы попытаетесь сделать коммит обычным способом (`git commit -m "..."`) с некорректным сообщением, система контроля отклонит его и укажет на ошибки.

### Создание новой версии (релиз)

Когда вы готовы выпустить новую версию (например, после завершения работы над фичей или исправления нескольких багов):

1.  Убедитесь, что вы находитесь на основной ветке (`main` или `master`) и все ваши изменения закоммичены.
2.  Запустите команду:
    ```bash
    npm run release
    ```
3.  Эта команда автоматически:
    - Проанализирует все коммиты с момента последнего релиза.
    - Определит новую версию проекта (патч, минор или мажор).
    - Обновит версию в `package.json`.
    - Сгенерирует и обновит файл `CHANGELOG.md`.
    - Создаст коммит с этими изменениями и Git-тег с номером новой версии.

4.  Чтобы опубликовать релиз в удаленном репозитории (например, на GitHub), выполните команду:
    ```bash
    git push --follow-tags
    ```
