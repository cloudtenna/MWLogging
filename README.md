MWLogging - simple wrapper macros around the ASL (Apple System Log).

See the blog post:

http://doing-it-wrong.mikeweller.com/2012/07/youre-doing-it-wrong-1-nslogdebug-ios.html


# APIs

_logFatal(format, ...)
_logError(format, ...)
_logWarn(format, ...)
_logInfo(format, ...)
_logDebug(format, ...)

# Build Settings

On your APPNAME-Prefix.pch

#include <asl.h>

#define MW_COMPILE_TIME_LOG_LEVEL ASL_LEVEL_DEBUG

Replace ASL_LEVEL_DEBUG by ASL_LEVEL_INFO, ASL_LEVEL_WARNING, ASL_LEVEL_ERR, ASL_LEVEL_EMERG accordingly to your build. I recommend set to ASL_LEVEL_ERR on PROD.
