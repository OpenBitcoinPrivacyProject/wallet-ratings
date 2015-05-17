Bitcoin Wallet Privacy Ratings Methodology
==========================================

Most of the criteria in the wallet ratings generate results in one of the following standard forms:

* Boolean (true/false)
* Number of clicks

Each result is converted to a numeric score between 0 and 100 via the methods described below. The criteria are designed such that a higher score is always better than a lower score.

When a test is not clearly applicable to a particular wallet because the wallet does not include the criteria tests, a score of either 0 or 100 is applied according to the following guidelines:

* If the test checks for the absence of undesirable behavior, and the wallet avoids the undesirable behavior for reasons unanticipated by the authors of the criteria, the item is scored at 100.
* If the test checks for the presense of desirable behavior, and the wallet achieves the same benefit of the desired behavior in methods unanticipated by the authors of the criteria, the item is scored at 100.
* In all other cases, the item is scored at 0.

## Boolean

* When the result of a test is true, that item is assigned a score of 100.
* When the result of a test is false, the item is assigned a score of 0.

## Number of clicks

The number of clicks needed to perform an action is converted to a score as follows:

100 * 2<sup>(<sup>-n</sup>/<sub>3</sub>)</sup>

where n is the number of clicks

* Zero clicks means the wallet achieves the desired behavior without any additional user action, which results in an item score of 100.
* Every three clicks drops the score by half.
* When the desired behavior can not be achieved in a particular wallet, the score is zero.
* If a particular action requires the user to type a command, each press of the space bar and return key counts as a click.
