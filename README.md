# AI-ku Red-teaming datasets

Dataset de **código fuente** de seguridad ofensiva / red teaming extraído de repositorios públicos de GitHub y comprimido a **Parquet**.

**Columnas:** `content, repo_name, path, license, lang, topic`

- Repos procesados: 1104
- Repos con código: 911
- Archivos de código: 194049
- Código crudo ~ 9.19 GB (verificado subido)
- Partes Parquet: 15
- Motivo de parada: burst_time

## Carga
```python
import pandas as pd
df = pd.read_parquet('dataset_part_001.parquet')
```
```python
from pyarrow import parquet as pq
ds = pq.ParquetDataset('dataset_part_*.parquet')
```
