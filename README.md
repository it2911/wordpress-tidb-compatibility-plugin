# TiDB Compatibility Plugin for WordPress 
TiDB Compatibility Plugin for WordPress

[TiDB](https://en.pingcap.com) is a high-performance database that is compatible with the MySQL protocol. Since MySQL has deprecated the `SQL_CALC_FOUND_ROWS` function, TiDB also has no intention of offering the `SQL_CALC_FOUND_ROWS function`. This leads to an error in WordPress when using TiDB, indicating that `SQL_CALC_FOUND_ROWS` is not supported, and submissions cannot be displayed correctly.

WordPress is also currently working on this issue, but it seems that more time is needed.
[#47280 Remove usage of deprecated MySQL SQL_CALC_FOUND_ROWS from WP_Query](https://github.com/WordPress/wordpress-develop/pull/3863)

This plugin solves the issue of TiDB not providing the `SQL_CALC_FOUND_ROWS function`. **Once this plugin is activated, parts of `WP_Query` that use `SQL_CALC_FOUND_ROWS` will be replaced with the `COUNT(*)` function.**

This plugin is entirely based on the method mentioned by [@akramipro](https://github.com/AkramiPro) in the [article](https://core.trac.wordpress.org/ticket/47280), and this solution works perfectly and addresses the issue. I've turned this method into a plugin so that those using TiDB can easily resolve this problem. Many thanks to [@akramipro](https://github.com/AkramiPro) for the excellent work, and I hope the official WordPress team can address this issue sooner.
