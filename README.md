# Android-Permission-Mappings
This repository contains permission mappings for Android API levels 16-33, primarily divided into three parts: SDK mappings, ContentProvider mappings, and Intent mappings. 

For more details, please refer to the following paper. Also, please cite this paper if you use these permission mappings:
```
@inproceedings{DBLP:conf/issre/YangBLGD24,
  author       = {Shishuai Yang and
                  Guangdong Bai and
                  Ruoyan Lin and
                  Jialong Guo and
                  Wenrui Diao},
  title        = {Beyond the Horizon: Exploring Cross-Market Security Discrepancies
                  in Parallel Android Apps},
  booktitle    = {Proceedings of the 35th {IEEE} International Symposium on Software Reliability Engineering,
                  {ISSRE} 2024, Tsukuba, Japan, October 28-31, 2024},
  pages        = {558--569},
  publisher    = {{IEEE}},
  year         = {2024},
  url          = {https://doi.org/10.1109/ISSRE62328.2024.00059},
  doi          = {10.1109/ISSRE62328.2024.00059},
  timestamp    = {Tue, 10 Dec 2024 13:47:38 +0100},
  biburl       = {https://dblp.org/rec/conf/issre/YangBLGD24.bib},
  bibsource    = {dblp computer science bibliography, https://dblp.org}
}
```
# Permission Annotation and Comments
Since Android 6.0 (API level 23), Google officially records permission mappings in two ways: (1) Using Java annotation @RequiresPermission("PermissionName") to associate API with permissions. (2) Using @link android.Manifest.permission#"Permission Name" to describe the permissions required to call this API in the comments.
# SDK Mappings
The SDK Mappings primarily include the mapping relationships between permissions and SDK APIs. We generate the complete SDK Mappings by combining two types of permission mappings: (1) Permission mappings extracted from permission annotations and comments, and (2) Permission mappings provided by [Axplorer](https://github.com/reddr/axplorer). For the detailed generation process, please refer to Section III-C of our paper "Beyond the Horizon: Exploring Cross-Market Security Discrepancies in Parallel Android Apps."
# ContentProvider Mappings and Intent Mappings
[Axplorer](https://github.com/reddr/axplorer) provides ContentProvider mappings for API levels 16 - 25. To obtain ContentProvider mappings for API levels 26 - 33, we retrieved all system ContentProviders protected by permissions from the source code of Android versions 8 - 13. For these ContentProviders, we extracted Content Uris and their corresponding permissions. Furthermore, we also extract Intent mappings from the source code of android.content.Intent class through annotation and comments. This class contains all Intent Actions along with required permissions.

