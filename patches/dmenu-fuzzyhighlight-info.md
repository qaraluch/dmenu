# extra step

To make this patch fully integrated with fuzzymatch and support 'case insensitive' features the following line must be changed:

if (*highlight == text[i]) {
into:

if (!fstrncmp(&(*highlight), &text[i], 1)) {
