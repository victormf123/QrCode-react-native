todo o codigo dessa jossa foi feito por min (y) .. e feio digitar isso ?! humm... por min que se foda sou eu que codifica msm rsrs.. pode falar nada, na real na real ninguem le essas merda não kkk então eu posso zoar o quanto eu quiser, por no final das contas eu ja sei as partes importantes kkkkkkk .. se fode ai kkkk aaah quero que entenda eu sou personagem, fruto da imaginação do meu caro programador ai... mais Shiiiiii e segredo :) hahahaHAHAHA ... medo o.0.


Então falando serio agora o desenvolvimento deste aplicativo foi feito usando um component chamado  react-native-camera o meu professor me deu uma dica de usar o zxing mas ao ler o README do app que estava em inglês(vale apena sitar// vcs jovens aprendam inglês, na moral vei... sei que e uma merda, mais vale muito a pena. ps: outro fruto da minha imaginação :), identifiquei que esse component foi descontinuado desde a versão 0.40.0, apos ler alguns foruns (todos em inglês --') descobri que dava para usar o component react-native-camerao link logo a seguir: https://github.com/lwansbrough/react-native-camera

Nesse componente tem um atributo chamado onBarCodeRead que vc declarndo uma função de forma que mostrarei a seguir, abrir o seu app np celular, gerar um qrcode pelo site http://br.qr-code-generator.com/a1/?PID=1150&kw=gerar%20um%20qr%20code&gclid=EAIaIQobChMI_v_lnqf21wIVSwmRCh3lZwsBEAAYASAAEgIpPvD_BwE, e colocar o sobre a tela do monitor o app le o qrcode e dispara um alerta.


//
     <Camera
          ref={(cam) => {
            this.camera = cam;
          }}
          style={styles.preview}
          aspect={Camera.constants.Aspect.fill}
          onBarCodeRead={this.onBarCodeRead.bind(this)}
          barCodeTypes={[
          	Camera.constants.BarCodeType.qr,
          ]}>
//
