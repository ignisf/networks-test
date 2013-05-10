Тестове
=======

Автоматизирана система за генериране на тестови варианти.

## Въвеждане на въпроси

Всеки въпрос се съдържа във файл в директорията `question_pool`. Файловите имена
на въпросите трябва да се разпознават от този регулярен израз:
`^[a-z0-9_-]+-[1-4]\.tex$`. Първата част на файловото име е уникален идентификатор
на въпрос, а втората – на вариант на въпроса. Пример: `nasko_15-1.tex`.

Самите въпроси се въвеждат по следните два шаблона:

За въпрос, чиито отговори са изредени един под друг:
```latex
\question[10] One of these things is not like the others; one of these things is
not the same. Which one is different?
\begin{choices}
  \choice John
  \choice Paul
  \choice
  George
  \choice Ringo
  \CorrectChoice Socrates
\end{choices}
```

За въпрос, чиито отговори са изредени един до друг (по-компактно):
```latex
\question[10] One of these things is not like the others; one of these things is
not the same. Which one is different?
\begin{oneparchoices}
  \choice John
  \choice Paul
  \choice George
  \choice Ringo
  \CorrectChoice Socrates
\end{oneparchoices}
```

Параметърът на `\question` е максималният брой точки, които могат да се получат от верен отговор на въпроса. С `CorrectChoice` се означава верния(те) отговор(и).

## Повече информация

http://www-math.mit.edu/~psh/exam/examdoc.pdf

http://en.wikibooks.org/wiki/LaTeX/Teacher%27s_Corner
