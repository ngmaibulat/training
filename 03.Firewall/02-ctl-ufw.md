### Install

```
sudo npm i -g @aibulat/ctl-ufw
```

### Prepare input file

Create a json file with list of allowed ports:

```json
[22, 25, 443]
```

Save the file, for example: fw.json

### Apply fw rules

```
sudo ctl-ufw fw.json
```
