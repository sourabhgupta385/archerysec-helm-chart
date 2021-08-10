# ArcherySec Helm Chart
A helm chart to install ArcherySec on OpenShift 4.x

## Usage

- Clone the repository
- Create service account and grant permissions
```
oc create sa archerysec-sa

oc adm policy add-scc-to-user anyuid -z archerysec-sa
```
- Install the helm chart

```bash
helm install archerysec .
```
- To upgrade archerysec helm release

```bash
helm upgrade archerysec .
```

- To delete archerysec instance

```bash
helm delete archerysec
```
## Notes

- If PVC storage is increased then pod must be restarted