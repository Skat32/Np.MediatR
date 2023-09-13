# Np.MediatR

Реалзирует в себе промежуточные слои для логирования и реакции на ошибки в сервисе который использует MediatR

Данный пакет использует [Np.Service.Report](https://gitlab.forta.local/development/nuget-packages/Np.Service.Report). Необходимо ознакомиться с инструкцией в нем

## Установка

Для начала надо зарегестрировать его в `ServiceCollectionExtensions.ConfigureApplicationServices()`

``` C#
        services.AddSingleton(typeof(IPipelineBehavior<,>), typeof(TimingsBehavior<,>));
        services.AddSingleton(typeof(IPipelineBehavior<,>), typeof(LoggingBehavior<,>));
```