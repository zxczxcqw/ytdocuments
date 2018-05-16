# ytdocuments
言通文档
```php
<?php
/**
 * Created by PhpStorm.
 * User: Administrator
 * Date: 2018/3/27
 * Time: 13:50
 */

namespace app\models;
use yii\db\ActiveRecord;


class Test extends ActiveRecord
{
     public function rules()
     {
         return [
             ['id','integer'],
             ['val','string','length'=>['0','6']]
         ];
     }
}

```
```js
const name = "zhangsan"
const arr = new Array()
arr.map((k, v)=>{
     console.log(k)
})
```
