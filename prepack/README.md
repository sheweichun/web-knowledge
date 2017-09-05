PreludeGenerator具备的方法

1. memoizeReference
2. convertStringToMember

3. globalReference





# prepack运行流程

1. 构建realm（contruct\_realm.js）
2. 初始化全局环境  （注意核心global.\_\_abstract,在intrinsics/global.js中）

```
export default function(realm: Realm): Realm {
  initializePrepackGlobals(realm);
  if (realm.isCompatibleWith("browser")) {
    initializeDOMGlobals(realm);
  }
  if (realm.isCompatibleWith(realm.MOBILE_JSC_VERSION)) {
    initializeReactNativeGlobals(realm);
  }
  return realm;
}
```

# 



