const accountSid = 'AC128981125229eb557ccf57f714a9669f';
const authToken = '[AuthToken]';
const client = require('twilio')(accountSid, authToken);

client.messages
    .create({
        body: 'Your appointment is coming up on July 21 at 3PM',
        from: 'whatsapp:+14155238886',
        to: 'whatsapp:+919582005146'
    })
    .then(message => console.log(message.sid))
    .done();