So... we cannot use nested string interpolations in expressions for now. It seems that we can use `format` instead: <https://github.community/t/nested-variable-substitution/140291>.

```none
Run echo ${FOOBAR}
  echo ${FOOBAR}
  shell: /usr/bin/bash -e {0}
  env:
    FOOBAR: 
    PIYO1: false
    PIYO2: true
    PIYO3: ${{ matrix.example }}
```

