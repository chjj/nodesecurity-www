---
title:  sequelize SQL Injection in Order
author:  Levan Basharuli
module_name: sequelize
publish_date: Sun Jan 18 2015 22:00:00 GMT-0800 (PST) 
cves: "[]"
vulnerable_versions: "<=2.0.0-rc7"
patched_versions: ">2.0.0-rc7"
...

## Overview

SQL Injection is possible in an application using the npm module sequelize if untrusted user input is passed into the order parameter.


Example:
```
Test.findAndCountAll({
where: { id :1 },
order : [['id', 'UNTRUSTED USER INPUT']]
})
```

## Recommendations

Upgrade to the [version on GitHub](https://github.com/sequelize/sequelize) until the latest version is pushed to npm.

## References
- https://github.com/sequelize/sequelize/issues/2906
