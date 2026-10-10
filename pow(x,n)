
from decimal import Decimal, localcontext

class Solution:
    def myPow(self, x, n):
        with localcontext() as ctx:
            ctx.prec = 60

            base = Decimal.from_float(x)
            exponent = abs(n)

            if n < 0:
                base = Decimal(1) / base

            result = Decimal(1)

            while exponent > 0:
                if exponent % 2 == 1:
                    result *= base

                base *= base
                exponent //= 2

            return float(result)
