<h1>CRV & veCRV FAQ</h1>

## **Какова цель и полезность CRV?** {#what-is-the-purpose-and-utility-of-crv}

Основные цели токена Curve DAO (CRV) заключаются в стимулировании поставщиков ликвидности на платформе Curve Finance, а также в привлечении как можно большего числа пользователей к участию в управлении протоколом.

Кроме того, CRV используется для голосования с учетом времени владения токенами (time-weighted voting) в процессе управления и дает возможность получать часть комиссий Curve Finance, генерируемых при блокировке токенов в форме veCRV.

## **Как получить CRV?** {#how-to-get-crv}

CRV можно приобрести двумя способами:

* Купить на рынке через биржу
* Получить в качестве вознаграждения за предоставление ликвидности в пулах или кредитных рынках Curve, которые предлагают вознаграждения в CRV. Это помогает протоколу продолжать предоставлять низкие комиссии и крайне низкое проскальзывание.

## **Где можно найти график выпуска?** {#where-can-i-find-the-release-schedule}

Вы можете найти график выпуска на следующие шесть лет по этому адресу в основном интерфейсе: [**https://dao.curve.fi/inflation**](https://dao.curve.fi/inflation)​.

Также имеется подробная документация в разделе [Объем и распределение CRV](./supply-distribution.md#crv-emissions-for-the-next-10-years) о эмиссии CRV на следующие 10 лет, а [калькулятор предложения](./supply-distribution.md#supply-calculator) можно использовать для просмотра эмиссии на любой год.

## **Какое текущее предложение в обращении?** {#what-is-the-current-circulating-supply}

Существует три способа проверить текущее предложение в обращении:

* В основном интерфейсе по адресу: [**https://dao.curve.fi/inflation**](https://dao.curve.fi/inflation).
* В [калькуляторе предложения](./supply-distribution.md#supply-calculator) просмотрев статистику за любой день.
* В [**on-chain контракте**](https://etherscan.io/address/0x14139EB676342b6bC8E41E0d419969f23A49881e) (`0x14139EB676342b6bC8E41E0d419969f23A49881e`), который показывает предложение в обращении за вычетом заблокированных или находящихся в вестинге токенов.

## **Когда был запущен CRV?** {#when-was-crv-launched}

CRV был официально запущен 13 августа 2020 года.

## **Что такое vote-locking CRV?** {#what-is-crv-vote-locking}

Vote-locking (блокировка для права голоса) относится к процессу блокировки CRV на определенный период, чтобы получить veCRV. Чем дольше вы блокируете, тем больше veCRV вы получаете. Vote-locking позволяет вам голосовать в управлении, увеличивать ваши вознаграждения CRV и получать торговые комиссии. **Vote locking boost означает**, что пользователи с veCRV (vote-locked CRV) получают увеличенные вознаграждения при предоставлении ликвидности в пуле или кредитном рынке.

!!!warning "veCRV не подлежит передаче"
    Когда вы блокируете свои токены CRV (vote-locking), вы получаете veCRV в количестве зависимом от длительности блокировки. Токены veCRV **не подлежат передаче**. После окончания периода блокировки пользователи могут вернуть свои токены CRV.

## **Что такое vote locking boost?** {#what-is-the-vote-locking-boost}

Когда вы осуществляете vote-locking CRV, вы также получаете boost за предоставленную ликвидность до 2,5x. Цель заключается в стимулировании пользователей участвовать в управлении, вознаграждая их большей долей ежедневной инфляции CRV. Подробнее [здесь](../reward-gauges/boosting-your-crv-rewards.md)

## **Когда начился boost?** {#when-did-the-boost-start}

Boost был впервые применен 26 августа 2020 года около 23:00 UTC.

## **Что такое veCRV?** {#what-are-vecrv}

veCRV означает "депонированный на голосование CRV" (voting escrow CRV). Это ваши заблокированные для голосования CRV. Чем дольше вы блокируете свои CRV, тем больше у вас voting power (сила голоса) и тем больший boost вы можете получить. Вы можете заблокировать 1000 CRV на год, чтобы получить вес 250 veCRV. Каждый CRV, заблокированный на четыре года, равен 1 veCRV.

Количество veCRV, которое вы получите, зависит от длительности блокировки ваших CRV. Минимальное время блокировки — одна неделя, а максимальное — четыре года.

Ваш вес (количество) veCRV постепенно уменьшается по мере приближения срока окончания блокировки ваших токенов. График, иллюстрирующий уменьшение, можно найти по адресу: [https://dao.curve.fi/locker](https://dao.curve.fi/locker)​

## **Как рассчитывается ваш boost?** {#how-is-your-boost-calculated}

Чтобы достичь максимального boost в 2.5x, необходимо учитывать несколько параметров. Формулу для увеличения можно увидеть [здесь](../reward-gauges/boosting-your-crv-rewards.md#formula)

Вы можете найти текущую voting power (силу голоса) DAO по этому адресу: [https://dao.curve.fi/locker](https://dao.curve.fi/locker)​

**Вы также можете найти калькулятор по этому адресу:** [https://dao.curve.fi/minter/calc](https://dao.curve.fi/minter/calc)​

## **Что, если я предоставляю ликвидность в нескольких пулах?** {#what-if-i-provide-liquidity-in-multiple-pools}

Ваша voting power (сила голоса) применяется ко всем cчётчикам вознаграждений (gauges), но может давать разный boost в зависимости от того, сколько ликвидности вы предоставляете и сколько общей ликвидности в пуле.

## **Что происходит, если больше людей блокируют CRV?** {#what-happens-if-more-people-vote-lock}

Если другие поставщики ликвидности блокируют больше CRV, ваш boost останется таким, каким оно был, когда вы его применили. Если вы злоупотребляете этим, другой пользователь может вмешаться и обновить ваш boost до реального уровня.

## **Как часто мой boost учитывает изменения voting power?** {#how-often-does-my-boost-records-voting-power-changes}

Ваша voting power уменьшается со временем, но ваш boost будет учитывать уменьшение voting power (силы голоса) только на определенных контрольных точках, таких как депозит, вывод в счётчик вознаграждений (gauges) или выпуск (minting) CRV.

Например, если вы начинаете с 1000 veCRV, и ваша voting power со временем уменьшается до 800 veCRV, ваш boost все равно будет использовать исходную силу голоса в 1000 veCRV до следующей контрольной точки пользователя.

## **Как применить мой boost?** {#how-can-i-apply-my-boost}

После создания или добавления к вашей блокировке вам нужно нажать кнопку применения увеличения, чтобы обновить ваш boost для каждого cчётчика вознаграждений (gauge), в котором вы предоставляете ликвидность. Ваш boost также может быть обновлен путем депозита или вывода из cчётчика вознаграждений (gauge).

Нажмите на ссылку ниже, чтобы ознакомиться с руководством по блокировке и увеличению вознаграждений CRV:

[Увеличение (Boosting) ваших вознаграждений CRV](../reward-gauges/boosting-your-crv-rewards.md)

## **Как узнать, активен ли мой boost?** {#how-to-know-my-boost-is-active}

Если ваш boost отображается, значит он активен.

Если вы заблокировали CRV, но ваш boost не отображается, вам нужно его применить.

## **Как работает ежегодное сокращение эмиссии?** {#how-does-the-yearly-emissions-reduction-work}

Сокращение эмиссии может быть инициировано любым пользователем после истечения периода времени (точно 365 дней) с момента последнего сокращения эмиссий. Это делается путем вызова функции `update_mining_parameters` в контракте `CRV` по адресу [`0xD533a949740bb3306d119CC777fa900bA034cd52`](https://etherscan.io/token/0xD533a949740bb3306d119CC777fa900bA034cd52).

Когда это вызывается, начинается новая эпоха, запускающая еще 365 дней. Если никто не вызывает эту функцию, CRV продолжает эмитироваться по текущей ставке, и новая эпоха не запускается. Например, если это вызвано на 1 день позже, это повлияет на две важные функции:

* Предложение CRV будет выше теоретического максимума в 3,030,303,031.8 CRV
* Следующее сокращение эмиссий будет отложено на 1 день, так как обратный отсчет 365 дней начинается на 1 день позже.

Это также означает, что каждый раз, когда происходит високосный год, дата, когда можно сократить эмиссии, будет сдвинута вперед на один день в году.

## **Как выпускаются токены CRV?** {#how-is-crv-minted}

CRV может быть создан пользователями, которые стейкают в cчётчиках вознаграждений (gauges) после того, как в счётчики было выделенно CRV для чеканки. Когда это происходит, токены CRV создаются, добавляются к общему предложению и передаются пользователю.

Если пользователи решат не выпускать (выводить награды) сразу, это может создать расхождение между теоретическим предложением токенов и реальным предложением токенов, отображаемым на блок-эксплорерах.
