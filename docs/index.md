![logo do projeto](assets/logo.png){width="300" .center}
# Notas musicais

Notais musicais é um CLI para ajudar na formação de escalas e acordes

Temos dois comandos disponíveis: `escala` e `acorde`

## como usar?

### Escalas

Você pode chamar as esclas via linha de comando. Por exemplo:

```bash
poetry run escala
```

Retornando os graus e nptas correspondentes a essa escala:

```bash
┏━━━┳━━━━┳━━━━━┳━━━━┳━━━┳━━━━┳━━━━━┓
┃ I ┃ II ┃ III ┃ IV ┃ V ┃ VI ┃ VII ┃
┡━━━╇━━━━╇━━━━━╇━━━━╇━━━╇━━━━╇━━━━━┩
│ C │ D  │ E   │ F  │ G │ A  │ B   │
└───┴────┴─────┴────┴───┴────┴─────┘
```

#### Alteração na escala

O primeiro parâmetro do CLI é a tônica da escala que deseja exibir. Dessa forma você pode alterar a escala retornada. Por exemplo, a escala de `F#`:
```bash
poetry run escala F#
```

Resultado em: 

```bash
┏━━━━┳━━━━┳━━━━━┳━━━━┳━━━━┳━━━━┳━━━━━┓
┃ I  ┃ II ┃ III ┃ IV ┃ V  ┃ VI ┃ VII ┃
┡━━━━╇━━━━╇━━━━━╇━━━━╇━━━━╇━━━━╇━━━━━┩
│ F# │ G# │ A#  │ B  │ C# │ D# │ F   │
└────┴────┴─────┴────┴────┴────┴─────┘
```

#### Alteração na tonalidade da escala

Você pode alterar a tonalidade da escala também! Esse é o segundo parâmetro da linha de comando. Por exemplo, a escala de `D#` maior:

```bash
poetry run escala D# menor

┏━━━━┳━━━━┳━━━━━┳━━━━┳━━━━┳━━━━┳━━━━━┓
┃ I  ┃ II ┃ III ┃ IV ┃ V  ┃ VI ┃ VII ┃
┡━━━━╇━━━━╇━━━━━╇━━━━╇━━━━╇━━━━╇━━━━━┩
│ D# │ F  │ G   │ G# │ A# │ C  │ D   │
└────┴────┴─────┴────┴────┴────┴─────┘
```

### Acordes

Uso básico

```bash
poetry run notas-musicais acorde

┏━━━┳━━━━━┳━━━┓
┃ I ┃ III ┃ V ┃
┡━━━╇━━━━━╇━━━┩
│ C │ E   │ G │
└───┴─────┴───┘
```

#### Variações na cifra

```bash
poetry run notas-musicais acorde C+

┏━━━┳━━━━━┳━━━━┓
┃ I ┃ III ┃ V+ ┃
┡━━━╇━━━━━╇━━━━┩
│ C │ E   │ G# │
└───┴─────┴────┘
```


## Mais informações sobre o CLI

Para descobrir outras opções, você pode usar a flag `--help`:

```bash
poetry run escala --help


 Usage: escala [OPTIONS] [TONICA] [TONALIDADE]                                                      
                                                                                                     
╭─ Arguments ────────────────────────────────────────────────────────────╮
│   tonica          [TONICA]      Tônica da escala [default: c]          |
│   tonalidade      [TONALIDADE]  Tonalidade da escala [default: maior]  │
╰────────────────────────────────────────────────────────────────────────╯
```