Yii Namespaced
==============
coding with `namespace` on Yii 1.x framework<br/>
multiple sites shared `lib` and `Yii framework`<br/>
multiple entries demo<br/>
namespaced model generator integrated to `gii`<br/>
support environment-based config

Project Struct
--------------
Path | Remark
-----|-------
yii | Yii 1.x framework
_doc | documents
└─&ensp;db_demo.sql | demo database sql
lib | 
├─&ensp;constant | 
├─&ensp;models | 
│&ensp;&ensp;├─&ensp;BaseActiveRecord.php | extend Yii `CActiveRecord`, a little improved for AR
│&ensp;&ensp;└─&ensp;demo | `Database Name`
│&ensp;&ensp;&ensp;&ensp;&ensp;├─&ensp;dao | base model class, class name start with `_`, overwrite by namespaced model generator
│&ensp;&ensp;&ensp;&ensp;&ensp;└─&ensp;domain | model class, extend base model class at `dao`, for custom code, never be overwrited
├─&ensp;site | 
└─&ensp;yii | 
&ensp;&ensp;&ensp;└─&ensp;gii | 
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;└─&ensp;nsModel | namespaced model generator
site_demo | demo site
├─&ensp;entry | 
│&ensp;&ensp;├─&ensp;dev | folder for entry `dev.php`
│&ensp;&ensp;│&ensp;&ensp;├─&ensp;config | 
│&ensp;&ensp;│&ensp;&ensp;├─&ensp;controllers | 
│&ensp;&ensp;│&ensp;&ensp;├─&ensp;views | 
│&ensp;&ensp;│&ensp;&ensp;└─&ensp;runtime | yii framework required
│&ensp;&ensp;└─&ensp;index |folder for entry `index.php`
│&ensp;&ensp;&ensp;&ensp;&ensp;├─&ensp;config | 
│&ensp;&ensp;&ensp;&ensp;&ensp;├─&ensp;controllers | 
│&ensp;&ensp;&ensp;&ensp;&ensp;├─&ensp;views | 
│&ensp;&ensp;&ensp;&ensp;&ensp;└─&ensp;runtime | yii framework required
└─&ensp;_root_ | web root
&ensp;&ensp;&ensp;├─&ensp;assets | yii framework required
&ensp;&ensp;&ensp;├─&ensp;dev.php | entry `dev.php`
&ensp;&ensp;&ensp;└─&ensp;index.php | entry `index.php`
