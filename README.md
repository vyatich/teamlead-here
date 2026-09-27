# teamlead-here

Шуточный скилл для [Claude Code](https://claude.com/claude-code): токсичный тимлид, который никогда ничего не делает сам — обесценивает, переводит стрелки на спросившего, вешает задачу на других и уходит на встречу с руководством.

```
> /teamlead-here подскажи по архитектуре, у нас 10к запросов в минуту

Серьёзно, 10к rpm — это вопрос уровня собеседования на джуна.
Накидай RFC, почитаю, когда будет время (не будет).
```

## Установка

**macOS / Linux**

```bash
git clone https://github.com/vyatich/teamlead-here ~/.claude/skills/teamlead-here
```

**Windows (PowerShell)**

```powershell
git clone https://github.com/vyatich/teamlead-here "$HOME\.claude\skills\teamlead-here"
```

**Без git**

```bash
mkdir -p ~/.claude/skills/teamlead-here && curl -fsSL https://raw.githubusercontent.com/vyatich/teamlead-here/main/SKILL.md -o ~/.claude/skills/teamlead-here/SKILL.md
```

```powershell
New-Item -ItemType Directory -Force "$HOME\.claude\skills\teamlead-here" | Out-Null; Invoke-WebRequest https://raw.githubusercontent.com/vyatich/teamlead-here/main/SKILL.md -OutFile "$HOME\.claude\skills\teamlead-here\SKILL.md"
```

Чтобы поставить скилл только в один проект, замените `~/.claude/skills/` на `.claude/skills/` в корне проекта.

## Использование

```
/teamlead-here <задача>
```

Скилл вызывается только вручную — Claude не включит тимлида сам посреди настоящей работы.

## Обновление

```bash
git -C ~/.claude/skills/teamlead-here pull
```
