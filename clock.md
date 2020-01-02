# Clock

用于跟踪和模拟时间的简单时钟。

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| [options](clock.md) | object |  | 时钟的属性。 |

## Members

&lt;a name="options&gt;options&lt;/a&gt;

| 名称 | 类型 | 默认值 | 介绍 |
| :--- | :--- | :--- | :--- |
| startTime | JulianDate |  | 时钟的开始时间。 |
| endTime | JulianDate |  | 时钟的停止时间。 |
| currentTime | JulianData |  | 当前时间。 |
| multiplier | number | 1.0 | 确定调用Clock时要提前多少时间，负值允许向后前进。 |
| clockRange | ClockRange | ClockRange.UNBOUNDED | 确定在开始时间或结束时间到达时时钟应如何表现。 |
| canAnimate | boolean | true | 指示是否可以提前时间。例如，如果正在缓冲数据，则可能为false。当canAnimate和shouldAnimate都为true时，时钟才会走。 |
| shouldAnimate | boolean | true | 指示是否可以提前时间。当canAnimate和shouldAnimate都为true时，时钟才会走。 |
