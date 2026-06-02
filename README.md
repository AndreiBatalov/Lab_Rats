# Lab_Rats

Проект по анализу медицинских изображений (крыса, IPPG / кардиосинхронизация).

Архив с данными: https://drive.google.com/file/d/13nrIEdfUKkIHkBxOZvM-tff_gHaFRExj/view?usp=sharing

## Окружение

```bash
conda activate change_detector
pip install -r requirements_pip.txt
```

## Пайплайн

| Этап | Где | Результат |
|------|-----|-----------|
| 0–1 | [`lab_rats.ipynb`](lab_rats.ipynb) | `PHASE1_*.txt` |
| 2 | ноутбук, `RUN_PHASE2=True` при пересчёте | `PHASE2_cardio_cycles.txt` |
| 4–7 | [`lab_rats.ipynb`](lab_rats.ipynb), ячейки после этапа 2 | `PHASE3_*` … `PHASE6_*` |

```bash
conda activate change_detector
# этапы 4–7: выполнить ячейки 8–18 в lab_rats.ipynb по порядку
```

Кадр `n` → `1-1/rat8s6e1/F{1+(n-1)//3000}/img_{n:09d}.png`

Конфиг ROI: [`roi_config.json`](roi_config.json). Описание шагов: [`pipeline.txt`](pipeline.txt).
