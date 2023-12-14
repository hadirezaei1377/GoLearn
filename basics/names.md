names in golang divided to two categories:
public (exportable) and private (non-exportable)

exportability: have an access from outside of the package to its functions, variables, attributes, etc.
Try to always write private unless it needs to be accessible from outside.
If the first letter is capitalized, it means public.
