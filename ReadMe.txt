#--------------------------------------------------------------------------------------------------
# ReadMe.txt
# 	Seo-Eun Choi sc214782@uw.edu
# 	last updated: 2020.03.19.
#--------------------------------------------------------------------------------------------------

# Specification:
	R 3.6.1  with MplusAutomation 0.7-3


# This folder contains three folders, as
	1 Language
	2 VSP


# Method:
	Item-bank-approach was used.
	Some ADNI language items are different from phase to phase.
		Category-Vegetable	: ADNI 1 only			(item name : catvegesc)
		MoCA (6 items)		: ADNI 2/GO 3 only		(item names: lion, camel, rhino, repeat1, repeat2, ffluency)
		BNT total		: ADNI 1, 2/GO only		(item name : bnttotal)


	Process in four steps:
		(1) Fit a model with people whose baseline visits were with ADNI 1. Obtain item parameters. 
		    Mean and variance of latent variable are set to 0 and 1, respectively.

		(2) Fit a model with people whose baseline visits were with ADNI 2/GO,3, fixing item parameters from (1).
		    Mean and variance of latent variable are freely estimated.

		(3) Fit a model with all visits, fixing item parameters from (1) and (2).
		    Mean and variance of latent variable are freely estimated.

		(4) Fit a model with all visits, fixing item parameters from (1) and (2), fixing mean and variance of latent variable. 
		    Obtain composite scores.

	Remark:
	ADNI-VSP items are the same over phases; however, the same approach was used to be consistent.
	(baseline only, then all visits)

