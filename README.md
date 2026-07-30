# Trills
A new project exploring "Trills" and what their implementation might look like.

To begin, I'll explain what a "Trill" is, who came up with them, where I heard about them, and what this project entails exactly.

A Trill is a proposed perpetual bond that is issued by governments that pays an annual coupon equal to one trillionth of the issuing nation's GDP. It allows individual citizens to have a literal vested interest in the future prosperity of their (or another) nation. The biggest selling point is that governments can avoid issuing debts in the form of bonds and instead exchange "equity" for shares of the nation's GDP much in the same way a business issues shares as a means to raise capital.

Trills are the brainchild of Nobel Laureate Robert Shiller and his partner Mark Kamstra. The two have been espousing the benefits of Trills for over 16 years having published a paper titled ["The Case for Trills: Giving the People and Their Pension Funds a Stake in the Wealth of the Nation"](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=1444351) in 2009. There have been several papers on Trills over the years, but the concept never took off. I read about them for the first time last year when reading Andrew W Lo and Stephen R Foerster's book "In Pursuit of the Perfect Portfolio" wherein they interview the preeminent minds in the world of finance. Among those they interview is Robert Shiller and he discusses the Trill in the book.

In reading the chapter with Shiller, I was intrigued by the concept and wondered what a Trill would be worth. Calculating the value could prove tricky. You would use CAPM presumably, but how does one reliably forecast a nation's GDP? In this project, I'll explore how I went about calculating the NPV of a Trill and some of the overlooked downsides of the proposed financial instrument.

I utilized the Capital Asset Pricing Model (CAPM) along with NPV calculations, Gordon's Growth Model for long-term growth, and a Random Forest ML algorithm that was fed data from the World Bank API to try and estimate the key economic variables for the equations. The end results were very interesting:

### CAPM Parameters
| Parameter | Value |
| :--- | :--- |
| **Risk-Free Rate** | 4.28% |
| **Market Return** | 9.97% |
| **Trill Beta** | -0.0171 |
| **Discount Rate** | 4.18% |


### Results
| Metric | Value |
| :--- | :--- |
| **Projected Trill Dividend (Year 1)** | $27.83 |
| **NPV of Next 30 Years** | $677.67 |
| **Discounted Terminal Value** | $1,950.11 |
| **ESTIMATED FAIR VALUE OF 1 US TRILL** | **$2,627.78** |

I think it's important to also discuss the downsides of Trills. There are some pretty glaring deficiencies in the system and reasons why Trills haven't been adopted. 

- Trills would be less convenient, safe, or reliable than treasury bonds due to their direct ties to the GDP. People buying bonds want consistent coupons, but Trills don't offer that. 

- There is a concern of Moral Hazard when it comes to the reporting of the GDP if Trills factor into the country's debt.

- While Trills would soften economic hardships (lower GDP, lower payments), it also softens economic booms (higher GDP, higher payments).

Ultimately, while Trills are a fascinating theoretical tool that could effectively hedge inflation and stabilize debt during hardships, the political and financial costs during times of prosperity make them a tough sell.

**Python Stack:**

pandas, numpy, yfinance, sklearn
