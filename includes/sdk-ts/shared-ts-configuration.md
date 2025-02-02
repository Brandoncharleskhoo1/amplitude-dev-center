???config "Configuration Options"
    | <div class="big-column">Name</div>  | Description | Default Value |
    | --- | --- | --- |
    |`apiKey`| Required. `string`. The apiKey of your project. | `null` | 
    |`flushIntervalMillis`| `number`. The amount of time waiting to upload the event to the server in millionseconds. | 1 second.|
    |`flushQueueSize`| `number`. The maximum number of events that can be stored locally before forcing an upload.  | 30 events. |
    |`flushMaxRetries`| `number`. The max retry limits. | 5 times.|
    |`logLevel`| `LogLevel.None` or `LogLevel.Error` or `LogLevel.Warn` or `LogLevel.Verbose` or `LogLevel.Debug`. The log level. | `LogLevel.Warn` |
    |`loggerProvider`| `Logger`. Implements a custom `loggerProvider` class from the Logger, and pass it in the configuration during the initialization to help with collecting any error messages from the SDK in a production environment.| `Amplitude Logger` |
    |`minIdLength`| `number`. Overrides the minimum length of `user_id` & `device_id` fields. | `5` |
    |`optOut`| `boolean`. If `optOut` is `true`, the event isn't sent to Amplitude's servers. | `false` |
    |`serverUrl`| `string`. The server url events upload to. | `https://api2.amplitude.com/2/httpapi` | 
    |`serverZone`| `EU` or  `US`. Set Amplitude Server Zone, switch to zone related configuration. To send data to Amplitude's EU servers should configure to `EU` | `US` |
    |`storageProvider`| `Storage<Event[]>`. Implements a custom `storageProvider` class from Storage. | `MemoryStorage` |
    |`useBatch`| `boolean`. When `true`, uses the Batch API instead of the HTTP V2 API.| `false` |
    |`transportProvider`| `Transport`. Custom HTTP client. For example, sending requests to your proxy server with customized HTTP request headers.| `Transport` |
    |`transport`| `TransportType.XHR` or `TransportType.SendBeacon` or `TransportType.Fetch`. Set the transport type. | `TransportType.Fetch` |