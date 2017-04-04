# Plot Related

<!-- > Created by Fisher at 03:54 on 2017-03-30. -->

```matlab
plot(x, y)

% Draw the points.
scatter(x, y)

% Hold the current figure.
hold on

% Grid the figure.
grid on

% Set labels.
xlabel('Some Label for X')
ylabel('Some Label for Y')
title('Figure Title')

% Add legend and specify the position.
legend('Data','Slope','Slope & Intercept','Location','best');

% Set x tick frequency.
set(gca,'xtick',1:5:60);
% Set x tick label
set(gca,'xticklabel',1:5:60);
```
