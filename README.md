# Run esmini V1.0.0
A custom github action to ease runing simulations in the open source scenario simulator [esmini](https://esmini.github.io/).

## Usage
Use this github action in a github actions pipeline as follows:

Using **minimal** inputs parameters:

```yaml
steps:
  - name: run esmini simulation
    uses: localhorst87/run-esmini@v1.0.0
    with:
        token: ${{ github.token }}
        xosc: ./scenarios/ALKS_cut-out.xosc
```

Using **all** inputs parameters:

```yaml
steps:
  - name: run esmini simulation
    uses: localhorst87/run-esmini@v1.0.0
    with:
        token: ${{ github.token }}
        xosc: ./scenarios/ALKS_cut-out.xosc
        parameter-variation: ./scenarios/cut-out-variation.xosc
        release: 2.26.2
        asset: esmini-demo_Linux.zip
        result-dir: ./esmini-res
        timestep: 0.02
```

## Inputs

See the [action script](./action.yml) for details