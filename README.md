# JQ Action

Process a value with a jq script and output to a step output.

## Inputs

### `input`

**Required** The input value to be processed by script.

### `script`

**Required** The JQ script.

### `compact`

Set to `"true"` to emit compact output from jq.

### `raw-output`

Set to `"true"` to have jq emit raw strings.

## Outputs

### `output`

The output of the JQ script.

## Example usage

```yaml
uses: edwardgeorge/jq-action@main
with:
  input: "[{\"num\": 1}, {\"num\": 2}]"
  script: "[.[] | select(.num == 1) | .num]"
```
