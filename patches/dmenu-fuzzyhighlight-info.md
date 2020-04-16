# extra step

To make this patch fully integrated with fuzzymatch and support 'case insensitive' features the following line must be changed:

For this case it will be in: dmenu.c file
line no.: 134

if (*highlight == text[i]) {
into:

if (!fstrncmp(&(*highlight), &text[i], 1)) {
