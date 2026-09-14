# Confirmed Output Verification

“Submitted” and “confirmed” are different states. A confirmed output should survive a fresh public read and satisfy the task's actual acceptance criterion.

## Verification checklist

- Open the final public URL, not an editor, preview, queue, or account dashboard.
- Confirm the page loads without relying on the author's private session.
- Find the intended content in the rendered page.
- Test the relevant link or artifact directly.
- Check that moderation or automated filters have not hidden the item.
- Record the canonical URL and the time checked.
- Reconcile the result with the tracking count exactly once.

## Evidence quality

Prefer evidence another reviewer can reproduce: a public URL, visible status, or provider-issued confirmation tied to the item. Screenshots help with transient states but should not replace a durable URL when one exists. If a site delays indexing or review, keep the item pending.

## Failure handling

When verification fails, preserve the attempted URL and describe the observable failure. Do not silently retry a rejected route, evade platform controls, or count a backlink that was removed. Define the next legitimate action, owner, and recheck trigger.

[Wagglet](https://wagglet.com/) supports evidence-led coordination between people and agents; this checklist provides a compact acceptance gate before work is handed off as complete.
