<h1>Создание пула Stableswap-NG</h1>

Создание пула Stableswap подходит для активов, которые, как ожидается, будут иметь привязку цен очень близко друг к другу, например, пары стейблкоинов. Мастер создания проведет вас через процесс создания пула, но если у вас возникнут вопросы, рекомендуется обратиться к члену команды Curve в [**Telegram**](https://t.me/curvefi) или [**Discord**](https://discord.gg/rgrfS7W).

Пулы Stableswap — это пулы ликвидности, содержащие **до восьми токенов** с использованием алгоритма StableSwap (Curve V1). Для лучшего понимания Curve V1, пожалуйста, смотрите здесь: [**Понимание Curve V1**](../base-features/understanding-curve.md).

!!!info "Stableswap-NG"
    StableSwap-NG — это усовершенствованная версия первой реализации StableSwap. Он сильно оптимизирован по газу и также включает динамические комиссии, которые возрастают  по мере увеличения использования ликвидности.

---

## **Токены в пуле** {#tokens-in-pool}

Вкладка выбора токенов может быть использована для выбора **от двух до восьми токенов**. Токен можно выбрать, выполнив поиск по символу любого токена, который уже используется на Curve, или вставив адрес пула. Дополнительные токены можно добавить с помощью синей кнопки **`Add token`**.

При создании метапула можно выбрать только два токена. Один из них — LP токен, а другой — токен для его пары.

!!!warning
    - **`ERC20:`** Пользователям рекомендуется тщательно проверять ERC20 токены, с которыми они взаимодействуют, так как этот контракт **не может различать безвредные и вредоносные** ERC20 токены.
    - **`Oracle:`** При использовании токенов с оракулами важно знать, что они **могут контролироваться извне с помощью EOA.**.
    - **`Rebasing:`** Пользователям и интеграторам рекомендуется понимать, как контракт AMM работает с перебазированием балансов (Rebasing).
    - **`ERC4626:`** Некоторые реализации ERC4626 **могут быть подвержены атакам на донаты/инфляцию**. Пользователям рекомендуется действовать с осторожностью.

---

*Чтобы AMM работал корректно, при выборе активов необходимо выбрать соответствующий им тип. Поддерживаются следующие типы активов:*

### **Стандартный ERC-20** {#standard-erc20}

Стандартные ERC-20 токены не требуют дополнительной конфигурации.

<figure markdown="span">
  ![](../images/pool_creation/ss_erc20_dark.png#only-dark){ width="400" }
  ![](../images/pool_creation/ss_erc20_light.png#only-light){ width="400" }
  <figcaption></figcaption>
</figure>



### **Токены с оракулами** {#tokens-with-oracles}

!!!warning "Точность оракула"
    Точность оракула ставки **должна быть $10^{18}$**. В противном случае пул ликвидности не будет функционировать корректно, так как обменный курс будет нарушен.

Некоторые токены могут требовать внешнего оракула курса для обеспечения корректных расчетов внутри AMM. Это особенно полезно для токенов с курсами относительно их базовых токенов, таких как rETH относительно ETH. В этом случае, при выборе токена с оракулом необходимо поставить галочку, и появится дополнительный раздел для адреса контракта и метода получения цены от оракула. Некоторые токены могут получать цену своего оракула из контракта, отличного от контракта токена.

<figure markdown="span">
  ![](../images/pool_creation/ss_oracle_dark.png#only-dark){ width="400" }
  ![](../images/pool_creation/ss_oracle_light.png#only-light){ width="400" }
  <figcaption></figcaption>
</figure>



### **Токены с ребейзом** {#rebasing-tokens}

Токены с ребейзом в криптовалюте — это криптовалюты, которые автоматически корректируют свое предложение периодически на основе заранее определенного алгоритма, обычно для поддержания стабильной стоимости или пега к другому активу.

<figure markdown="span">
  ![](../images/pool_creation/ss_rebasing_dark.png#only-dark){ width="400" }
  ![](../images/pool_creation/ss_rebasing_light.png#only-light){ width="400" }
  <figcaption></figcaption>
</figure>



### **ERC-4626** {#erc4626}

ERC-4626 — это стандарт, разработанный для оптимизации и унификации технических параметров доходных хранилищ. Он предоставляет стандартный API для токенизированных доходных хранилищ, которые представляют собой доли одного базового токена стандарта ERC-20. При использовании таких токенов пул рассчитывает базовую сумму, как если бы базовые токены находились в пуле.

<figure markdown="span">
  ![](../images/pool_creation/ss_erc4626_dark.png#only-dark){ width="400" }
  ![](../images/pool_creation/ss_erc4626_light.png#only-light){ width="400" }
  <figcaption></figcaption>
</figure>


---

## **Параметры** {#parameters}

*Stableswap-NG предлагает три различных стандартных пресета параметров пула:*

<figure markdown="span">
  ![](../images/pool_creation/ss_presets_dark.png#only-dark){ width="400" }
  ![](../images/pool_creation/ss_presets_light.png#only-light){ width="400" }
  <figcaption></figcaption>
</figure>


---

<figure markdown="span">
  ![](../images/pool_creation/ss_parameters_advanced_dark.png#only-dark){ width="400" }
  ![](../images/pool_creation/ss_parameters_advanced_light.png#only-light){ width="400" }
  <figcaption></figcaption>
</figure>


- **`Swap Fee ranging from 0% to 1%`**: Комиссия за своп, взимаемая во время транзакций.
- **`A ranging from 1 to 5,000`**: `A` — это коэффициент усиления, который определяет глубину ликвидности пула. Чем выше значение `A`, тем глубже ликвидность.
- **`Offpeg Fee Multiplier from 0 to 12.5`**: Множитель, который регулирует комиссию за своп в зависимости от состояния пула.
- **`Moving Average Time ranging from 60 to 3600 seconds`**: Временное окно скользящего среднего для встроенного оракула.

!!!info "`Offpeg Fee Multiplier`"
    
    Stableswap-NG вводит **динамическую комиссию**. Использование `Offpeg Fee Multiplier` позволяет системе динамически регулировать комиссию в зависимости от состояния пула.
    
    Инструмент для экспериментов с динамической комиссией: [https://www.desmos.com/calculator/zhrwbvcipo?](https://www.desmos.com/calculator/zhrwbvcipo?)
    


---

## **Информация о пуле** {#pool-info}

Наконец, после настройки всех параметров, можно выбрать **`Pool Name`** и **`Pool Symbol`**:

<figure markdown="span">
  ![](../images/pool_creation/ss_info_dark.png#only-dark){ width="400" }
  ![](../images/pool_creation/ss_info_light.png#only-light){ width="400" }
  <figcaption></figcaption>
</figure>


---

## **Развертывание пула** {#deploying-the-pool}

С правой стороны находится вкладка, которая суммирует всю информацию о токенах и параметрах нового пула. Пул наконец-то можно развернуть, нажав синюю кнопку **`Create Pool`** внизу.

<figure markdown="span">
  ![](../images/pool_creation/ss_summary_dark.png#only-dark){ width="300" }
  ![](../images/pool_creation/ss_summary_light.png#only-light){ width="300" }
  <figcaption></figcaption>
</figure>

После развертывания заложите первоначальную ликвидность и, возможно, вам стоит [**создать гейдж**](../reward-gauges/creating-a-pool-gauge.md) для начисления эмиссии CRV и других стимулов.
