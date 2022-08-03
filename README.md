# DDD
DDD（领域驱动设计）思想解读及优秀实践 学习笔记 附上视频下载地址

## DDD（领域驱动设计）思想解读及优秀实践 学习笔记 附上视频下载地址

### 下载地址：**[download](https://cowcowit.com/course/135/mksz541)**

随着全行业互联网化的深入，项目所涉及的业务越来越多样、精细、专业，普通的CRUD、传统架构模式与建模方法已无法满足市场需求。在此背景下，DDD思想再次受到大厂关注与欢迎。但是，市面上很多DDD课程不够落地，大家付出大量时间还是学得云里雾里。
BAT资深架构师，以一个DDD研发实战为主线，带你从概念到代码，真正吃透DDD。


```

@RestController
@RequestMapping("/commodity")
public class CommodityController {

  @Autowired
  private CommodityService commodityService;

  @RequestMapping(value = "/detail/{commodityId}", method = RequestMethod.GET)
  @ResponseBody
  public CommonResponse<CommodityInfoDto> getDetail(@PathVariable String commodityId) {
    CommodityInfoDto commodityInfoDto = commodityService.getCommodityDetail(commodityId);
    return CommonResponse.success(commodityInfoDto);
  }

  @RequestMapping(value = "/list", method = RequestMethod.POST)
  @ResponseBody
  public CommonResponse<List<CommodityInfoDto>> getCommodityList(@RequestBody
      ListCommodityByIdQueryDto request) {
    return CommonResponse.success(commodityService.getCommodityList(request.getIds()));
  }
}
```
![在这里插入图片描述](http://typora-markdown-2022.oss-cn-shanghai.aliyuncs.com/uPic/2022/08/04/1e277b1cba6a4bd5979270e8ccca09ec.png)

### 下载地址：**[download](https://cowcowit.com/course/135/mksz541)**

