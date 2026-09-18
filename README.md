# AI-ku Red-teaming datasets

Dataset de **código fuente** de seguridad ofensiva / red teaming extraído de repositorios públicos de GitHub y comprimido a **Parquet**.

**Columnas:** `content, repo_name, path, license, lang, topic`

- Repos procesados: 152
- Repos con código: 0
- Archivos de código: 0
- Código crudo ~ 14.68 GB (verificado subido)
- Partes Parquet: 33
- Motivo de parada: terminado_seguro

## Carga
```python
import pandas as pd
df = pd.read_parquet('dataset_part_001.parquet')
```
```python
from pyarrow import parquet as pq
ds = pq.ParquetDataset('dataset_part_*.parquet')
```
