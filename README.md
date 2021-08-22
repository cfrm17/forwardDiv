# Forward Dividend Calculator

FinPricing

Forward dividends are also called expected future dividends, or projected dividend, or implied dividends. They are critical for valuing any equity products. In other words, the key factor for pricing equity products is to correctly calculate equity forward taking all dividends into account. The stock price is adjusted by dividends over ex-dividend dates. 

An equity model must account for all the dividend payments between valuation date and the option maturity date. Those dividends are forward (or future or projected or implied) dividends. FinPricing provides tools for computing forward dividends based on market prices. Those dividends will allow you to match market quotes, expectations, and forecasting. By using the implied forward dividends, you can archive risk neutral or no arbitrage valuation.

Dividends tend to reduce the price of a stock on ex-dividend date by the amount of the dividend. All the equity models need to be adjusted to allow for the payout of dividends. There are three types of dividends: constant dividend yield, term structure of dividend yields, and term structure of discrete dividends.

Under constant dividend yield assumption, a stock pays dividend continuously. Ex-dividend dates are ignored. The forward price formula under constant dividend yield approach is very simple as

F=Se (r-q) (T-t)				(1)
where F is the forward price, S is the spot price, r is the interest rate, q is dividend yield, and (T-t) is time to maturity.


Under discrete dividend assumption, a stock price needs to be adjusted by all the dividends between the deal date and the product maturity date. The forward price under discrete dividend assumption can be expressed as


S_T=[S-PV(D)] e^(r_T (T-t) )  			(2)
where
	t – the valuation date
	T – the maturity date
	r – the interest rate between t and T
	S – the spot stock price
	PV(D)=∑_(t<τ<T)▒〖d_τ e^(-r_τ (τ-t) ) 〗   - the present value of all dividends 					   between t and T
d_τ – the discrete dividend paid at τ where t ≤ τ ≤ T

The term structures of dividend yields and discrete dividends are theoretically equivalent. The piece-wise dividend yields allow you to select the corresponding dividend yield based on maturity. An example of dividend yields is shown below.
2005-03-01	0.0441
2005-04-30	0.0220
2005-06-29	0.0293
2005-08-28	0.0327
2005-10-27	0.0262
2006-01-25	0.0268
2006-04-25	0.0278
2006-07-24	0.0285
2006-10-22	0.0290
2007-01-20	0.0293
2007-04-20	0.0300
2007-07-19	0.0305
2007-10-17	0.0309
2008-01-15	0.0312
2008-04-14	0.0320
2008-10-11	0.0332

If you have an outstanding option matures at 2005-7-15. You can choose the yield as 0.0293 (at 2005-06-29 for piece-wise assumption) and then use the forward formula under yield assumption as.
F_T=S_t e^((r-q_i)(T-t))				(3)

References:

https://finpricing.com/lib/ToolEqDiv.html

https://fliphtml5.com/download/download-pdf-file.php?str=x0DZh9GTud3bENXamIDM2QTN1QTPkl0av9mY
