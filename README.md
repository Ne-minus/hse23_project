# hse23_project
## Белковые выравнивания
Выравнивание проводилось в программе MEGA, использованный алгоритм -- ClustalW.  
**Гистон H2A**
![](https://github.com/Ne-minus/hse23_project/blob/main/data/screenshots/h2a_clust.png)
Последовательности похожи между собой. Несмотря на отсутствие * сверху (они указывают, если во всех последовательностях в данно позиции находится одна и та же аминокислота), визуально заметно явное сходство, а также видно, что в каждой позиции замены есть в небольшом количестве последовательностей (от 1 до 5) --> можно выбрать любую последовательность для данного гистона.  

**Гистон H2B**
![](https://github.com/Ne-minus/hse23_project/blob/main/data/screenshots/h2b_clust.png)
Здесь последовательности более похожи, на что указывает увеличение количества звездочек. Визуально также понятно, что последовательности "синонимичны".  

**Гистон H3**
![](https://github.com/Ne-minus/hse23_project/blob/main/data/screenshots/h3_clust.png)
Здесь почти во всех позициях у всех последовательностей стоит одна и та же аминокислота (большое количество звездочек) --> последовательности ОЧЕНЬ похожи.  

**Гистон H4**
![](https://github.com/Ne-minus/hse23_project/blob/main/data/screenshots/h4_clust.png)
Ситуация аналогична ситуации с гистном H3.

## Blast
Затем был проведен анализ гомологов(программа BLAST), а также выбор последовательностей гистонов и автоматиечское составление таблиц с E-value -log(E-value). (см. [тетрадку](https://github.com/Ne-minus/hse23_project/blob/main/table.ipynb)) 
## Результаты
Нелогарифмированные результаты:  
![](https://github.com/Ne-minus/hse23_project/blob/main/data/screenshots/no_log.png)  
Натуральный логарифм:  
![](https://github.com/Ne-minus/hse23_project/blob/main/data/screenshots/log.png)  

**Логариифм с основанием 10:**  
![](https://github.com/Ne-minus/hse23_project/blob/main/data/screenshots/log10.png)

## Heatmap
Код посмотрения см. в [тетрадке](https://github.com/Ne-minus/hse23_project/blob/main/table.ipynb)
Натуральный логарифм:  
![](https://github.com/Ne-minus/hse23_project/blob/main/data/screenshots/heatmap.png)
Логариифм с основанием 10:  
![](https://github.com/Ne-minus/hse23_project/blob/main/data/screenshots/heatmap_log10.png)
## Выводы
- чем дальше от текущего момента, тем меньше становится наша метрика (и, соответственно, увеличивается E-value), что представляется логичным -- более сложные структуры появляются постепенно -- от примитивных организмов к более развитым
- в каком-то виде UTY появляется уже у c.elegans(нематода -- беспозночное, эукариот)
- у организмов сложнее (см. тепловую карту) уже устойчиво имеется данный ген (однако UCSC бразуер подтверждает это только для мыши и человек, возможно, для дрозофилы и данио-рерио(zebrafish). Также возникло предположение, что такие хорошие результаты для дрозофилы и данио-рерио были получены за счет возможного наличия гомологов гена UTY на chrX (так как BLAST как раз ищет гомологичные последовательности))
