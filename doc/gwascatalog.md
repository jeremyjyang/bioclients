# `bioclients.gwascatalog`

## GWAS Catalog (The NHGRI-EBI Catalog of human genome-wide association studies)

[GWAS Catalog](https://www.ebi.ac.uk/gwas/) REST API client.

__Version 1:__
 * _"V1 was retired in August 2026."_
 * <https://www.ebi.ac.uk/gwas/docs/api>
 * <https://www.ebi.ac.uk/gwas/rest/api>
 * <https://www.ebi.ac.uk/gwas/rest/docs/api>
 * <https://www.ebi.ac.uk/gwas/rest/docs/sample-scripts>

__Version 2:__
 * _"GWAS RESTful API V2 has been released with various enhancements & improvements over GWAS RESTful API V1. REST API v2 is the only currently supported version of the GWAS Catalog API."_
 * <https://www.ebi.ac.uk/gwas/rest/api/v2/docs>
 * <https://www.ebi.ac.uk/gwas/rest/api/v2/docs/reference>
 * <https://www.ebi.ac.uk/gwas/docs/programmatic-access/rest-api/>


## Example commands

```
python3 -m bioclients.gwascatalog.Client list_studies_v2 --o gwascatalog_studies.tsv
```

```
python3 -m bioclients.gwascatalog.Client get_studyAssociations_v2 --ids "GCST004364,GCST000227"
```

```
python3 -m bioclients.gwascatalog.Client get_snps_v2 --ids "rs6085920,rs2273833,rs6684514,rs144991356"
```

```
python -m bioclients.gwascatalog.Client -h
usage: Client.py [-h] [--ids IDS]
                 [--searchtype {pubmedmid,gcst,efotrait,efouri,accessionid,rs}]
                 [--i IFILE] [--o OFILE] [--skip SKIP] [--nmax NMAX]
                 [--api_host API_HOST]
                 [--api_base_path_v1 API_BASE_PATH_V1]
                 [--api_base_path_v2 API_BASE_PATH_V2] [-v] [-q]
                 {get_metadata,get_metadata_v1,get_metadata_v2,list_studies,list_studies_v1,list_studies_v2,get_studyAssociations,get_studyAssociations_v1,get_studyAssociations_v2,get_snps,get_snps_v1,get_snps_v2,search_studies_v1}

GWAS Catalog REST API V2 (V1-deprecated) client

positional arguments:
  {get_metadata,get_metadata_v1,get_metadata_v2,list_studies,list_studies_v1,list_studies_v2,get_studyAssociations,get_studyAssociations_v1,get_studyAssociations_v2,get_snps,get_snps_v1,get_snps_v2,search_studies_v1}
                        operation

options:
  -h, --help            show this help message and exit
  --ids IDS             IDs, comma-separated
  --searchtype {pubmedmid,gcst,efotrait,efouri,accessionid,rs}
                        ID type
  --i IFILE             input file, IDs
  --o OFILE             output (TSV)
  --skip SKIP
  --nmax NMAX
  --api_host API_HOST
  --api_base_path_v1 API_BASE_PATH_V1
  --api_base_path_v2 API_BASE_PATH_V2
  -v, --verbose
  -q, --quiet

Example PMIDs: 28530673; Example GCSTs: GCST004364, GCST000227;
Example EFOIDs: EFO_0004232; Example SNPIDs: rs6085920, rs2273833,
rs6684514, rs144991356
```
