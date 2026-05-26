*Trecho FASTA do transcritoma*

```         
>transcrito_exemplo_01
ATGCTAGCTACGATCGATCGTACGATGCTAGCTAGGCTAACGTTAGCTAGCTTACGATCGATCGGATCCGATGCTAGCTAACCGTACGATCGTTA
```

*Reads simulados — 35 pb*

```         
>read_01
ATGCTAGCTACGATCGATCGTACGATGCTAGCTA

>read_02
GATCGTACGATGCTAGCTAGGCTAACGTTAGCTA

>read_03
CTAGGCTAACGTTAGCTAGCTTACGATCGATCGGA

>read_04
TAGCTAGCTTACGATCGATCGGATCCGATGCTA

>read_05
ATCGGATCCGATGCTAGCTAACCGTACGATCGTTA

>read_06
GCTAACCGTACGATCGTTA
```

*Como seria o mapeamento??*
Transcrito:

```         
ATGCTAGCTACGATCGATCGTACGATGCTAGCTAGGCTAACGTTAGCTAGCTTACGATCGATCGGATCCGATGCTAGCTAACCGTACGATCGTTA
1        10        20        30        40        50        60        70        80        90        100
```

Mapeamento dos reads:

```         
read_01   1-35    ATGCTAGCTACGATCGATCGTACGATGCTAGCTA
read_02  21-55                        TACGATGCTAGCTAGGCTAACGTTAGCTA
read_03  36-70                                       GGCTAACGTTAGCTAGCTTACGATCGATCGGA
read_04  51-84                                                      AGCTAGCTTACGATCGATCGGATCCGATGCTA
read_05  67-101                                                                     TCGGATCCGATGCTAGCTAACCGTACGATCGTTA
read_06  82-101                                                                                    GCTAACCGTACGATCGTTA
```

Observação: na lista anterior, o read_04 tem 34 pb, não 35 pb. Uma versão corrigida com 35 pb seria:

```         
read_04  TAGCTAGCTTACGATCGATCGGATCCGATGCTAG
```
