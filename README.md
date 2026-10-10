# secom-tableau-dashboard
## Why these six sensors?

SECOM has 590 sensors (446 after cleaning), which is too many for one dashboard.
I picked 6, and the choice is meant to tell one story, not to be a complete ranking.

In my [SECOM analysis project](https://github.com/yuning777/secom-process-analysis) I tested every sensor for a difference
between passed and failed samples. Most failures happened in the first weeks, and many
sensors also drift over time, so I tested again after removing the slow drift from each sensor.

- **sensor_59, sensor_477, sensor_205**: still differ between pass and fail after removing the
  drift. They were the top 3 in that test, but the signal is weak (AUC about 0.61).
- **sensor_103, sensor_510, sensor_129**: ranked in the top 10 before removing the drift, but fell
  to rank 57-78 after. They look related to failure mostly because they drift over time,
  and failures were more common early on.

Switching between them in the dashboard shows the difference. Other sensors, like
sensor_341 and sensor_336, were almost as good as the top 3, so this is a choice for the
story, not proof that only these six matter. Nothing here shows that a sensor causes a failure.
