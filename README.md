# AI-ku Red-teaming datasets

Dataset de **código fuente** de seguridad ofensiva / red teaming extraído de repositorios públicos de GitHub y comprimido a **Parquet**.

**Columnas:** `content, repo_name, path, license, lang, topic`

- Repos procesados: 1043
- Repos con código: 567
- Archivos de código: 55675
- Código crudo ~ 5.02 GB (verificado subido)
- Partes Parquet: 7
- Motivo de parada: completado

## Carga
```python
import pandas as pd
df = pd.read_parquet('dataset_part_001.parquet')
```
```python
from pyarrow import parquet as pq
ds = pq.ParquetDataset('dataset_part_*.parquet')
```
