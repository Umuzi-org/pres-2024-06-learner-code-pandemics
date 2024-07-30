### example of a bad test:

```python
from unittest import TestCase
from unittest.mock import Mock
from mymodule import process_order

class TestProcessOrder(TestCase):
    def test_process_order(self):
        payment_gateway_mock = Mock()
        payment_gateway_mock.authorize.return_value = True
        payment_gateway_mock.charge.return_value = True
        payment_gateway_mock.refund.return_value = False  # Unnecessary mock

        result = process_order(payment_gateway=payment_gateway_mock, order_id=123, amount=100)
        
        self.assertTrue(result)
        payment_gateway_mock.authorize.assert_called_once()
        payment_gateway_mock.charge.assert_called_once()
```