| Comando    | Modo de Vim al que afecta                | Descripción rápida                             |
| ---------- | ---------------------------------------- | ---------------------------------------------- |
| `noremap`  | Normal, Visual, Select, Operator-pending | Equivale a `nnoremap + vnoremap + onoremap`    |
| `nnoremap` | Normal                                   | Modo más común para navegación y edición       |
| `vnoremap` | Visual + Select                          | Afecta selecciones visuales                    |
| `xnoremap` | Visual (exclusivamente)                  | Solo visual, no select                         |
| `snoremap` | Select                                   | Modo de selección tipo insertar (poco usado)   |
| `inoremap` | Insert                                   | Durante escritura                              |
| `cnoremap` | Command-line                             | Cuando estás escribiendo un comando (`:`)      |
| `onoremap` | Operator-pending                         | Tras comandos como `d`, `y`, `c`, etc.         |
| `lnoremap` | Lang-Arg (solo en algunas versiones)     | Modo de argumento de lenguaje, raramente usado |
| `tnoremap` | Terminal                                 | Modo terminal (Neovim principalmente)          |
