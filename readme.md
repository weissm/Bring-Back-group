## Bring Back group.all_x

Home Assistant release 0.104 removed the automatically generated entity groups (`group.all_*`) 😢

If like me, you used `group.all_x` for your automation, this appdaemon app lets you bring back the generated entity groups you need.

## Installing

Install via [HACS](https://hacs.xyz/). Alternatively, place the apps folder and its contents in your appdaemon folder.

## Configuration
| Variable | Type   | Required | Default | Description          |
|----------|--------|----------|---------|----------------------|
| module   | string | TRUE     |         | Set to `bbgax`       |
| class    | string | TRUE     |         | Set to `group_all_x` |
| domains  | list   | TRUE     |         | List of device groups you want to generate. <br/>Valid list options are: `automation`, `cover`, `device_tracker`, `fan`, `light`, `lock`, `plant`, `remote`, `script`, `switch`, `vacuum` |
  
### Example Usage
```yaml
any_name_you_wish:
  module: bbgax
  class: group_all_x
  domains: 
    - device_tracker
    - light
    - switch
```

<hr>

<a href="https://www.buymeacoffee.com/so3n" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;" ></a>