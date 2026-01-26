[# FAST_UWB_Combine
用于500米口径球面射电望远镜(FAST)超宽带数据拼接的Python程序]
(https://img.shields.io/badge/FAST-500m%2520Aperture%2520Spherical%2520Telescope-blue
https://img.shields.io/badge/python-3.9%252B-blue
https://img.shields.io/badge/license-MIT-green
https://img.shields.io/badge/built%2520with-astropy-orange
用于500米口径球面射电望远镜(FAST)超宽带数据拼接的Python程序。

该程序将UWB1、UWB2、UWB3、UWB4四个子波段的观测数据合并为连续的宽带数据。

核心功能

    自动化文件组识别：智能识别符合FAST命名模式的数据文件

    频率拼接校准：精确对齐并拼接相邻波段的频谱数据

    数据裁剪与反转：按预设截断频率处理各波段数据

    FITS格式兼容：保持标准FITS格式，更新所有相关头信息

    质量验证：自动验证输出数据完整性和正确性

    批量处理：批量处理多个观测数据集

    详细日志记录：记录处理过程

技术特性

    语言：Python 3，依赖Astropy、NumPy等标准科学计算库

    容错机制：内置安全检查和异常处理，防止数据损坏

    命令行界面：提供灵活的参数配置和目录管理

    输出验证：自动检查输出文件完整性和数据维度

    内存映射：使用memmap处理大文件，减少内存占用

文件命名约定

    FAST超宽带观测原始文件名

处理流程

    扫描与分组：自动识别匹配的文件组

    参数提取：读取频率、带宽、通道数等关键参数

    数据处理：裁剪、反转并校准各波段数据

    数据拼接：沿频率轴拼接四波段数据

    头文件更新：更新FITS头文件反映合并后参数

    文件生成：输出合并后的FITS文件

    质量验证：验证输出数据完整性和正确性

 使用示例

# 处理指定目录下的UWB数据
python fast_uwb_stitch.py /path/to/uwb_data
# 指定输入和输出目录
python fast_uwb_stitch.py /path/to/input -o /path/to/output
# 显示详细输出
python fast_uwb_stitch.py /path/to/data -v

系统要求

    Python 3.9+

    Astropy ≥ 5.0

    NumPy = 1.24

    足够磁盘空间存放中间文件和输出

许可

本项目遵循FAST数据政策，仅供FAST合作者使用
  
使用时请遵守FAST数据管理政策

建议在处理关键数据前先用测试数据验证配置

对于科学发表，请引用相关参考文献)
