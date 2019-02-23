优先级
=========
(TODO: implement)

QUIC will use the HTTP/2 prioritization mechanism. Roughly,
a stream may be dependent on another stream. In this situation,
the "parent" stream should effectively starve the "child" stream.
In addition, parent streams have an explicit priority. Parent
streams should not starve other parent streams, but should make
progress proportional to their relative priority.

QUIC将使用HTTP / 2优先级排序机制。
粗略地说，流可能依赖于另一个流。
在这种情况下，“父”流应该有效地使“子”流饿死（strave）。
此外，父流具有明确的优先级。
父流不应该饿死（strave）其他父流，但应该取得与其相对优先级成比例的进度。
