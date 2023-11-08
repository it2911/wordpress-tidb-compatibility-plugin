## Archiving the it2911/wordpress-tidb-compatibility-plugin GitHub Repository

Dear Community,

I hope this message finds you well. I am writing to inform you that the repository [it2911/wordpress-tidb-compatibility-plugin](https://github.com/it2911/wordpress-tidb-compatibility-plugin) will be archived and all activities will be subsequently moved to the new repository [pingcap/wordpress-tidb-plugin](https://github.com/pingcap/wordpress-tidb-plugin).

### Why is this happening?
The transition is part of our efforts to centralize the development and maintenance of the WordPress TiDB compatibility plugin under the official [PingCAP](https://en.pingcap.com) umbrella. By moving to the [pingcap/wordpress-tidb-plugin](https://github.com/pingcap/wordpress-tidb-plugin) repository, we aim to ensure more consistent updates, dedicated resources, and a single point of reference for all contributors and users.

### What does this mean?
Once a repository is archived, it will become read-only. This means that no new issues, pull requests, or commits can be added to the project. The repository will still be accessible for reference purposes.

### Next Steps:
For all future activities, including issues and contributions, please use the new repository at [pingcap/wordpress-tidb-plugin]. We encourage you to clone or fork the new repository if you wish to continue contributing to the project.

### Timeline:
The archiving process will take place on 2023/11/8 20：00 JST, after which no new contributions will be accepted on the old repository.

We want to take this opportunity to thank you for your contributions to [it2911/wordpress-tidb-compatibility-plugin]. Your efforts have been invaluable to the project, and we look forward to your continued support at our new repository.

Should you have any questions or concerns regarding this transition, please do not hesitate to reach out.

----

## TiDB Compatibility Plugin for WordPress 
TiDB Compatibility Plugin for WordPress

[TiDB](https://en.pingcap.com) is a high-performance database that is compatible with the MySQL protocol. Since MySQL has deprecated the `SQL_CALC_FOUND_ROWS` function, TiDB also has no intention of offering the `SQL_CALC_FOUND_ROWS function`. This leads to an error in WordPress when using TiDB, indicating that `SQL_CALC_FOUND_ROWS` is not supported, and submissions cannot be displayed correctly.

WordPress is also currently working on this issue, but it seems that more time is needed.
[#47280 Remove usage of deprecated MySQL SQL_CALC_FOUND_ROWS from WP_Query](https://github.com/WordPress/wordpress-develop/pull/3863)

This plugin solves the issue of TiDB not providing the `SQL_CALC_FOUND_ROWS function`. **Once this plugin is activated, parts of `WP_Query` that use `SQL_CALC_FOUND_ROWS` will be replaced with the `COUNT(*)` function.**

This plugin is entirely based on the method mentioned by [@akramipro](https://github.com/AkramiPro) in the [article](https://core.trac.wordpress.org/ticket/47280), and this solution works perfectly and addresses the issue. I've turned this method into a plugin so that those using TiDB can easily resolve this problem. Many thanks to [@akramipro](https://github.com/AkramiPro) for the excellent work, and I hope the official WordPress team can address this issue sooner.
