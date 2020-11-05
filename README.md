# webgl-gpu-power-estimation-data

Repository of data scraped from various GPU benchmark websites and associated scripts that can be used with the [webgl-gpu-power-estimation](https://github.com/gkjohnson/webgl-gpu-power-estimation/) module. GPU benchmark and spec information scraped from:

- [videocardbenchmark.net](https://www.videocardbenchmark.net/GPU_mega_page.html)
- [techpowerup.com](https://www.techpowerup.com/gpu-specs/)
- [notebookcheck.net](https://www.notebookcheck.net/Mobile-Graphics-Cards-Benchmark-List.844.0.html).

## License Information

The scraped graphics card data provided in this repo is subject to the terms of the respective websites. Data and scripts are available to use as long as the data source and ownership are acknowledged. Repo contents should not be distributed in separate packages.

## Database Information

The `database.json` object stores a database with scraped GPU names as keys and objects with database information as values which can be used by the [webgl-gpu-power-estimation](https://github.com/gkjohnson/webgl-gpu-power-estimation/) utility. Where performance information is not consistently provided between websites an interpolated value is generated. The following data is generated and reported for each entry:

```js
{

  // Name of the GPU
  name,

  // Type of graphics card
  // Workstation, Desktop, Mobile, Unknown
  type,

  // The 3d and 2d performance results as provided by the
  // PassMark g3d and g2d benchmarks
  performance,

  // thermal design power
  tdp,

  // total available vram in MB
  memory,

  // clock speeds in MHz
  clock,
  memoryClock

}
```
