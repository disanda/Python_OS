# logging 库

- 记录日志用的，可以输出到命令行，也可以输出到文件

- 输出有四个级别： DEBUG < INFO < WARNING < ERROR < CRITICAL

```
import logging

logger = logging.getLogger('aaa')

logging.debug('aaa')
logging.info('bbb')
logging.warning('ccc')


logger.setLevel(logging.debug)
```
