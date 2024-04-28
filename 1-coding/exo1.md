/**
 * @param {number} millis
 * @return {Promise}
 */
async function sleep(millis) {
    let start = Date.now()
    let now = Date.now()
    while (now - start < millis) {
        now = Date.now()
    }
    return true
}
