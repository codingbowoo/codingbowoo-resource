> 파일 이름이 ```tex.md```인게 상당히 마음에 든다.


# 표
- 여러 열을 합하고 싶을 때
```tex
\multicolumn{2}{c|}{(1)}
```
> \multicolumn{몇 개의 열을 합할 것인가}{정렬은 어떻게?}{열 안에 넣을 내용(위의 예시에서는 (1))}


- 여러 행을 합하고 싶을 때 
```tex
\usepackage{multirow}

\multirow{2}{*}{(1)} & (이어지는 내용) & ...
 & (이어지는 내용)
```
> \multirow{몇 개의 행을 합할 것인가}{*}{합친 행 안에 넣을 내용(위의 예시에서는 (1))}

마지막 줄을 보면 첫 칸을 비웠음(행을 합치지 않았다면 있었을 칸)을 확인할 수 있다. 
