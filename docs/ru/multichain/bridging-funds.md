Чтобы использовать Curve на цепочках, отличных от Ethereum, вам нужно _мостить_ средства на сайдчейн. Curve работает на нескольких цепочках, задокументированных здесь:

[Понимание мультичейна](../multichain/understanding-multichain.md)

Мосты не управляются Curve, поэтому Curve не может предложить поддержку по использованию мостов. Следующие проблемы могут повлиять на пользователей мостов, поэтому обязательно проведите исследование и проявляйте осторожность.

*   **Проблемы с ликвидностью:** Иногда у мостов недостаточно ликвидности для обработки транзакций. Обычно мост будет ждать пополнения ликвидности, прежде чем разрешит обработку средств.
*   **Застрявшие средства:** Иногда средства будут перемещены из одной цепочки, но не появятся в новой цепочке своевременно. Иногда это решается просто ожиданием. В крайних случаях вам следует обратиться в каналы поддержки соответствующего моста.
*   **Взломы:** Межцепочечная коммуникация может быть сложной, и мост является
