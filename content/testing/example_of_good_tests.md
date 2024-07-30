### Example of good tests

```python
from unittest import TestCase
from unittest.mock import create_autospec
from mymodule import process_order, PaymentGateway

class TestProcessOrder(TestCase):
    def test_process_order(self):
        payment_gateway_spy = create_autospec(PaymentGateway, instance=True)
        payment_gateway_spy.authorize.return_value = True
        payment_gateway_spy.charge.return_value = True

        result = process_order(payment_gateway=payment_gateway_spy, order_id=123, amount=100)
        
        self.assertTrue(result)
        payment_gateway_spy.authorize.assert_called_once()
        payment_gateway_spy.charge.assert_called_once()
```