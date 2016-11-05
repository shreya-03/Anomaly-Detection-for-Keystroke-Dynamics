# Comparing Anomaly-Detection Algorithms for Keystroke Dynamics

### What is keystroke dynamics (or keystroke biometrics)?

- study of whether people can be distinguished by their typing rhythms.

### Applications

- acting as an electronic fingerprint
- access-control and authentication mechanism
- detecting computer-based crimes

### Existing work
Comparing Anomaly-Detection Algorithms for Keystroke Dynamics
- http://www.cs.cmu.edu/~maxion/pubs/KillourhyMaxion09.pdf
- http://www.cs.cmu.edu/~keystroke/

### Data

The data are arranged as a table with 34 columns. Each row of data corresponds
to the timing information for a single repetition of the password by a single
subject. The first column, subject, is a unique identifier for each subject
(e.g., s002 or s057). Even though the data set contains 51 subjects, the
identifiers do not range from s001 to s051; subjects have been assigned unique
IDs across a range of keystroke experiments, and not every subject participated
in every experiment. For instance, Subject 1 did not perform the password
typing task and so s001 does not appear in the data set. The second column,
sessionIndex, is the session in which the password was typed
(ranging from 1 to 8). The third column, rep, is the repetition of the password
within the session (ranging from 1 to 50).

The remaining 31 columns present the timing information for the password. The
name of the column encodes the type of timing information. Column names of the
form H.key designate a hold time for the named key (i.e., the time from when
key was pressed to when it was released). Column names of the form
DD.key1.key2 designate a keydown-keydown time for the named digraph
(i.e., the time from when key1 was pressed to when key2 was pressed). Column
names of the form UD.key1.key2 designate a keyup-keydown time for the named
digraph (i.e., the time from when key1 was released to when key2 was pressed).
Note that UD times can be negative, and that H times and UD times add up to
DD times.

Consider the following one-line example of what you will see in the data:
  subject  sessionIndex  rep      H.period   DD.period.t   UD.period.t     ...
       s002             1    1        0.1491        0.3979        0.2488   ...
       The example presents typing data for subject 2, session 1, repetition 1.
       The period key was held down for 0.1491 seconds (149.1 milliseconds);
       the time between pressing the period key and the t key
       (keydown-keydown time) was 0.3979 seconds; the time between releasing
       the period and pressing the t key (keyup-keydown time) was
       0.2488 seconds; and so on.
