# Redis

## `func NewClient(logger *logrus.Logger, ctx context.Context, cancel context.CancelFunc) (*Client, error)`

NewClient initializes and returns a new Redis client.

 * **Parameters:**
   * `logger` — A logger instance for logging.
   * `ctx` — The context for the client operations.
   * `cancel` — A cancel function to stop the context.
 * **Returns:** A pointer to the initialized Client and an error if any occurred.

## `func (rc *Client) Instance() *redis.Client`

Instance returns the underlying Redis client instance.

 * **Returns:** A pointer to the Redis client.

## `func (rc *Client) Close() error`

Close closes the Redis client connection.

 * **Returns:** An error if closing fails.

## `func (rc *Client) InitializeStream() error`

InitializeStream initializes the Redis stream and consumer group.

 * **Returns:** An error if initialization fails.

## `func (rc *Client) Ping() error`

Ping checks the connection to Redis by sending a PING command.

 * **Returns:** An error if the ping fails.

## `func (rc *Client) PushToRedis(data map[string]interface`

PushToRedis adds data to the Redis stream.

 * **Parameters:** `data` — The data to be added to the stream.
 * **Returns:** An error if the operation fails.