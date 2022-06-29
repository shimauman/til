## Version
- 

## Patterns
```
- ab
    - sample1.ts

- abc
    - sample2.ts

- abd
    - sample3.ts

- cd
    - sample4.ts
```

#### `ab/sample1.ts`, `abc/sample2.ts`, `abd/sample3.ts`を得る
```
ab*/**/*.ts
```

#### `abc/sample2.ts`, `abd/sample3.ts`を得る
```
ab?/**/*.ts
```

#### `abc/sample2.ts`, `abd/sample3.ts`を得る
```
ab[a-z]/**/*.ts
```

#### `ab/sample1.ts`を得る
```
!(cd|ab?)/**/*.ts
```

#### 全てを得る
```
**/*.ts
```

## Use Case
ESlint/Prettierでチェックするディレクトリを指定する時に使用する。

## Reference
- 
